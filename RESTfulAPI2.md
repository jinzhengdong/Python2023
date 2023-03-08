# RESTful API

本节我们将基于SQL Server的用户表user，使用pyodbc提供用户跨域支持的以下服务：

* `/register`，post，用户注册服务
* `/login`，post，用户登录服务
* `/users`，get，获取所有用户信息
* `/users/{id}`，get，获取指定用户信息
* `/users/{id}`，put，修改指定用户信息
* `/users/{id}`，delete，修改指定用户信息

用户表user的DDL如下：

```ddl
create table user (
    id int identity(1, 1) not null primary key,
    username varchar(50) not null,
    password varchar(50) not null,
    email nvarchar(200) not null
)
```

## 条件

已经完成SQL Server安装。

## 安装必要的软件包

```bash
pip install pyodbc
pip install flask
pip install flask-cors
```

## npm安装

* 在浏览器中打开Node.js官网（https://nodejs.org/），下载最新的LTS版本的Node.js安装程序。
* 运行安装程序，按照默认设置完成Node.js的安装过程。注意，需要勾选“npm package manager”选项，以确保同时安装npm。
* 打开命令提示符或PowerShell终端，运行以下命令，验证Node.js和npm已经正确安装：

```bash
node -v
npm -v
```

## 实现服务

```python
import pyodbc
from flask import Flask, request, jsonify
from flask_cors import CORS

app = Flask(__name__)
CORS(app)  # 允许所有来源的跨域请求

# 数据库连接配置
server = 'localhost'
database = 'testdb'
username = 'sa'
password = 'password'
cnxn = pyodbc.connect(f'DRIVER=SQL Server;SERVER={server};DATABASE={database};UID={username};PWD={password}')

@app.route('/register', methods=['POST'])
def register():
    username = request.json['username']
    password = request.json['password']
    email = request.json['email']
    cursor = cnxn.cursor()
    cursor.execute('INSERT INTO User (username, password, email) VALUES (?, ?, ?)', (username, password, email))
    cnxn.commit()
    return jsonify({'message': 'User created successfully'})

@app.route('/login', methods=['POST'])
def login():
    username = request.json['username']
    password = request.json['password']
    cursor = cnxn.cursor()
    cursor.execute('SELECT * FROM User WHERE username = ? AND password = ?', (username, password))
    user = cursor.fetchone()
    if user:
        return jsonify({'message': 'Login successful'})
    else:
        return jsonify({'message': 'Invalid username or password'})

@app.route('/users', methods=['GET'])
def get_users():
    cursor = cnxn.cursor()
    cursor.execute('SELECT * FROM User')
    users = cursor.fetchall()
    return jsonify(users)

@app.route('/users/<int:id>', methods=['GET'])
def get_user(id):
    cursor = cnxn.cursor()
    cursor.execute('SELECT * FROM User WHERE id = ?', id)
    user = cursor.fetchone()
    if user:
        return jsonify(user)
    else:
        return jsonify({'message': 'User not found'})

@app.route('/users/<int:id>', methods=['PUT'])
def update_user(id):
    username = request.json['username']
    password = request.json['password']
    email = request.json['email']
    cursor = cnxn.cursor()
    cursor.execute('UPDATE User SET username = ?, password = ?, email = ? WHERE id = ?', (username, password, email, id))
    cnxn.commit()
    return jsonify({'message': 'User updated successfully'})

@app.route('/users/<int:id>', methods=['DELETE'])
def delete_user(id):
    cursor = cnxn.cursor()
    cursor.execute('DELETE FROM User WHERE id = ?', id)
    cnxn.commit()
    return jsonify({'message': 'User deleted successfully'})

if __name__ == '__main__':
    app.run(host='0.0.0.0', port=5000, debug=True)
```

## 前端项目初始化

进入前端项目目录`prjs\LPFrontEnd`并键入下面命令：

```bash
npm init
```

或者`npm init -y`也课创建需要的项目，完成项目初始化后，通过下面指令安装必要的前端脚本：

```
npm install jquery

npm instal layui
```

安装完成后引入下面相关脚本

```html
<!-- 引入jQuery -->
<script src="./node_modules/jquery/dist/jquery.min.js"></script>

<!-- 引入Layui -->
<link rel="stylesheet" href="./node_modules/layui-src/dist/css/layui.min.css">
<script src="./node_modules/layui-src/dist/layui.js"></script>
```

## 创建前端页面

进入`prjs\LPFrontEnd`目录并创建`login.html`:

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Login</title>
    <link rel="stylesheet" href="https://cdn.staticfile.org/layui/2.5.7/css/layui.min.css">
</head>
<body>

<div class="layui-container" style="margin-top: 30px;">
    <div class="layui-row">
        <div class="layui-col-md6 layui-col-md-offset3">
            <div class="layui-card">
                <div class="layui-card-header">Login</div>
                <div class="layui-card-body">
                    <form class="layui-form" lay-filter="login-form">
                        <div class="layui-form-item">
                            <label class="layui-form-label">Username</label>
                            <div class="layui-input-block">
                                <input type="text" name="username" lay-verify="required" placeholder="Enter username"
                                       autocomplete="off" class="layui-input">
                            </div>
                        </div>
                        <div class="layui-form-item">
                            <label class="layui-form-label">Password</label>
                            <div class="layui-input-block">
                                <input type="password" name="password" lay-verify="required" placeholder="Enter password"
                                       autocomplete="off" class="layui-input">
                            </div>
                        </div>
                        <div class="layui-form-item">
                            <div class="layui-input-block">
                                <button class="layui-btn" lay-submit lay-filter="login-form">Login</button>
                            </div>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </div>
</div>

<script src="https://cdn.staticfile.org/jquery/3.6.0/jquery.min.js"></script>
<script src="https://cdn.staticfile.org/layui/2.5.7/layui.min.js"></script>

<script>
    layui.use(['form'], function () {
        var form = layui.form;

        // 监听表单提交事件
        form.on('submit(login-form)', function (data) {
            // 发起登录请求
            $.ajax({
                url: '/login',
                type: 'POST',
                contentType: 'application/json',
                data: JSON.stringify(data.field),
                success: function (res) {
                    layer.msg(res.message);
                    // 登录成功后跳转到主页
                    window.location.href = '/index.html';
                },
                error: function (xhr, status, error) {
                    layer.msg(xhr.responseJSON.message);
                }
            });

            return false; // 阻止表单提交
        });
    });
</script>

</body>
</html>
```

## 用户注册页面

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Register</title>
    <link rel="stylesheet" href="https://cdn.staticfile.org/layui/2.5.7/css/layui.min.css">
</head>
<body>

<div class="layui-container" style="margin-top: 30px;">
    <div class="layui-row">
        <div class="layui-col-md6 layui-col-md-offset3">
            <div class="layui-card">
                <div class="layui-card-header">Register</div>
                <div class="layui-card-body">
                    <form class="layui-form" lay-filter="register-form">
                        <div class="layui-form-item">
                            <label class="layui-form-label">Username</label>
                            <div class="layui-input-block">
                                <input type="text" name="username" lay-verify="required" placeholder="Enter username"
                                       autocomplete="off" class="layui-input">
                            </div>
                        </div>
                        <div class="layui-form-item">
                            <label class="layui-form-label">Password</label>
                            <div class="layui-input-block">
                                <input type="password" name="password" lay-verify="required" placeholder="Enter password"
                                       autocomplete="off" class="layui-input">
                            </div>
                        </div>
                        <div class="layui-form-item">
                            <div class="layui-input-block">
                                <button class="layui-btn" lay-submit lay-filter="register-form">Register</button>
                            </div>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </div>
</div>

<script src="https://cdn.staticfile.org/jquery/3.6.0/jquery.min.js"></script>
<script src="https://cdn.staticfile.org/layui/2.5.7/layui.min.js"></script>

<script>
    layui.use(['form', 'layer'], function () {
        var form = layui.form;
        var layer = layui.layer;

        // 监听表单提交事件
        form.on('submit(register-form)', function (data) {
            // 发起注册请求
            $.ajax({
                url: '/register',
                type: 'POST',
                contentType: 'application/json',
                data: JSON.stringify(data.field),
                success: function (res) {
                    layer.msg(res.message);
                    // 注册成功后跳转到登录页面
                    window.location.href = '/login.html';
                },
                error: function (xhr, status, error) {
                    layer.msg(xhr.responseJSON.message);
                }
            });

            return false; // 阻止表单提交
        });
    });
</script>

</body>
</html>
```
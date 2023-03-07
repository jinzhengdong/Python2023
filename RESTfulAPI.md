# RESTful API

## pyodbc

在Windows上安装pyodbc：

* 打开命令提示符（Command Prompt）或PowerShell
* 如果你使用的是Python 3.4或更高版本，请确认已安装pip。在命令提示符或PowerShell中输入以下命令，如果已安装pip，将显示pip版本号：

```bash
pip --version
```

如果未安装pip，请先安装pip，可以在这里找到详细的安装步骤：https://pip.pypa.io/en/stable/installing/

* 在命令提示符或PowerShell中输入以下命令来安装pyodbc：

```bash
pip install pyodbc
```

## SQL Server

使用pyodbc执行语句返回受影响的行数。

```python
import pyodbc

def execute_sql(sql_query, connection_string):
    try:
        # 连接到数据库
        conn = pyodbc.connect(connection_string)
        cursor = conn.cursor()

        # 执行 SQL 语句
        cursor.execute(sql_query)
        row_count = cursor.rowcount

        # 提交事务并关闭连接
        conn.commit()
        conn.close()

        # 返回受影响的行数
        return row_count

    except pyodbc.Error as e:
        print(f"Error executing SQL query: {sql_query}")
        print(e)
        return None
```

```python
sql_query = "UPDATE Products SET Price = 10.99 WHERE Category = 'Toys'"
connection_string = "Driver={SQL Server};Server=server_name;Database=database_name;Trusted_Connection=yes;"

row_count = execute_sql(sql_query, connection_string)
print(f"{row_count} rows affected")
```

使用pyodbc执行查询并返回结果:

```python
import pyodbc

def execute_query(query_string):
    # 设置数据库连接参数
    conn_params = {
        'driver': '{SQL Server}',
        'server': 'your_server_name',
        'database': 'your_database_name',
        'uid': 'your_username',
        'pwd': 'your_password'
    }
    
    # 创建连接对象
    conn = pyodbc.connect(';'.join([f"{k}={v}" for k, v in conn_params.items()]))
    
    # 创建游标对象
    cursor = conn.cursor()
    
    # 执行查询
    cursor.execute(query_string)
    
    # 获取查询结果的列名
    columns = [column[0] for column in cursor.description]
    
    # 获取查询结果的所有行数据
    rows = cursor.fetchall()
    
    # 将查询结果转换成列表，每行数据作为一个字典
    result_set = [dict(zip(columns, row)) for row in rows]
    
    # 关闭游标和连接
    cursor.close()
    conn.close()
    
    # 返回查询结果
    return result_set
```

```python
result_set = execute_query("SELECT * FROM your_table_name")
print(result_set)
```

## My SQL

使用pyodbc:

```python
import pyodbc

def execute_sql(sql_query, connection_string):
    try:
        # 连接到数据库
        conn = pyodbc.connect(connection_string)
        cursor = conn.cursor()

        # 执行 SQL 语句
        cursor.execute(sql_query)
        row_count = cursor.rowcount

        # 提交事务并关闭连接
        conn.commit()
        conn.close()

        # 返回受影响的行数
        return row_count

    except pyodbc.Error as e:
        print(f"Error executing SQL query: {sql_query}")
        print(e)
        return None


sql_query = "UPDATE Products SET Price = 10.99 WHERE Category = 'Toys'"
connection_string = "DRIVER={MySQL ODBC 8.0 Unicode Driver};SERVER=localhost;DATABASE=mydatabase;USER=user;PASSWORD=password;"

row_count = execute_sql(sql_query, connection_string)
print(f"{row_count} rows affected")
```

使用`mysql.connector`执行查询并返回结果：

```python
import mysql.connector

def execute_query(query_string):
    # 设置数据库连接参数
    conn_params = {
        'host': 'your_host_name',
        'user': 'your_username',
        'password': 'your_password',
        'database': 'your_database_name'
    }
    
    # 创建连接对象
    conn = mysql.connector.connect(**conn_params)
    
    # 创建游标对象
    cursor = conn.cursor()
    
    # 执行查询
    cursor.execute(query_string)
    
    # 获取查询结果的列名
    columns = [column[0] for column in cursor.description]
    
    # 获取查询结果的所有行数据
    rows = cursor.fetchall()
    
    # 将查询结果转换成列表，每行数据作为一个字典
    result_set = [dict(zip(columns, row)) for row in rows]
    
    # 关闭游标和连接
    cursor.close()
    conn.close()
    
    # 返回查询结果
    return result_set
```

```python
result_set = execute_query("SELECT * FROM your_table_name")
print(result_set)
```

使用`pyodbc`执行查询并返回结果：

```python
import pyodbc

def execute_query(query_string):
    # 设置数据库连接参数
    conn_params = {
        'Driver': '{MySQL ODBC 8.0 Unicode Driver}',
        'Server': 'your_server_name',
        'Database': 'your_database_name',
        'UID': 'your_username',
        'PWD': 'your_password'
    }
    
    # 创建连接对象
    conn = pyodbc.connect(';'.join([f"{key}={value}" for key, value in conn_params.items()]))
    
    # 创建游标对象
    cursor = conn.cursor()
    
    # 执行查询
    cursor.execute(query_string)
    
    # 获取查询结果的列名
    columns = [column[0] for column in cursor.description]
    
    # 获取查询结果的所有行数据
    rows = cursor.fetchall()
    
    # 将查询结果转换成列表，每行数据作为一个字典
    result_set = [dict(zip(columns, row)) for row in rows]
    
    # 关闭游标和连接
    cursor.close()
    conn.close()
    
    # 返回查询结果
    return result_set
```

```python
result_set = execute_query("SELECT * FROM your_table_name")
print(result_set)

## Flask

```bash
pip install Flask

pip install flask-cors
```

API demo:

```python
from flask import Flask, jsonify
from flask_cors import CORS

app = Flask(__name__)
CORS(app)

@app.route('/')
def hello():
    return jsonify({'message': 'Hello, world!'})

if __name__ == '__main__':
    app.run()
```
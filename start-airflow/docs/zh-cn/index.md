# 概述
Apache Airflow 是一个用于编排和调度数据管道的开源平台。提供了一种简洁且可扩展的方式来定义、监控和管理工作流程。Airflow 主要用于数据工程、数据科学及与大规模数据处理相关的应用场景。

官方代码库：[https://github.com/apache/airflow](https://github.com/apache/airflow)

# 前置要求
1. 数据库可访问：在部署 Airflow 之前，需要先创建一个数据库以及 Airflow 将用于访问此数据库的数据库用户。

```bash
CREATE DATABASE airflow_db CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
CREATE USER 'airflow_user' IDENTIFIED BY 'airflow_pass';
GRANT ALL PRIVILEGES ON airflow_db.* TO 'airflow_user';
```

# 使用说明
1. 进入 Airflow 部署页面，按照提示填写部署参数：

![](https://img.alicdn.com/imgextra/i4/O1CN01LWSmJ71XE85FNE4Ai_!!6000000002891-2-tps-2626-1504.png)

2. 部署成功后，在已部署场景中，可以跳转查看目标 Airflow 应用

# 验证与使用
1. 部署成功后，访问 webserver CLB，可以看到登录界面

![](https://img.alicdn.com/imgextra/i4/O1CN01aZhBvI1aQRa2frm2i_!!6000000003324-2-tps-1314-362.png)

2. 输入用户名密码 airflow/airflow，登录成功后，可以看到 DAGs 运行界面.

![](https://img.alicdn.com/imgextra/i4/O1CN01rWN3Os23SO7RF0C3L_!!6000000007254-2-tps-2020-609.png)

3. 在 OSS 中上传 DAG python 文件

![](https://img.alicdn.com/imgextra/i4/O1CN016PlENf23JECIT8JQb_!!6000000007234-2-tps-453-341.png)

这里提供一个 DAG文件示例: task1 和 task2 都是 python 的任务

```python
from airflow import DAG
from airflow.operators.bash_operator import BashOperator
from airflow.operators.python_operator import PythonOperator
from datetime import datetime, timedelta

def my_python_function():
    print("Hello from Python!")


def my_python_function1():
    print("Hello from airflow!")

# 创建 DAG 对象
with DAG(
    "example_dag",
    schedule_interval='*/1 * * * *',  # 每天凌晨执行一次
    start_date=datetime(2022, 1, 1),
    catchup=False,
) as dag:
    task1 = PythonOperator(
        task_id="extract_data",
        python_callable=my_python_function1,
        dag=dag,
    )
    task2 = PythonOperator(
        task_id="my_python_task",
        python_callable=my_python_function,
        dag=dag,
    )
    task1 >> task2  # 定义任务的依赖关系
```
从 webserver 控制台中可以看到 task1 和 task2 两个任务

![](https://img.alicdn.com/imgextra/i1/O1CN010nwqhW24jAF4zf9ZQ_!!6000000007426-2-tps-1497-651.png)

4.触发上面创建的 DAG 任务运行，可以看到运行成功

![](https://img.alicdn.com/imgextra/i3/O1CN01YRmSXF1Tt73sPkc9K_!!6000000002439-2-tps-1224-716.png)

5.同时能在 sae-airflow-scheduler 应用实例看到实时运行的 Task Pod，在 Task 运行结束后会被自动删除
![](https://img.alicdn.com/imgextra/i3/O1CN01drKqln1OYR6QGvVWm_!!6000000001717-2-tps-1474-554.png)
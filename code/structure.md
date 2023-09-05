## STRUCTURE OF DAG FILE:

### IMPORT STATEMENTS:
     DAG file always starts with the import statements. Some main import statements includes the
                
                from airflow import DAG
                from airflow.decorators import task
                from airflow.operators.bash import BashOperator
                from airflow.operators.python import PythonOperator

### DAG DEFINITION:
     The nextstep is to define the DAG function using with or decorator or defining it directly.

#### WAYS OF DEFINING DAG:

##### 1. Using With DAG:  
     with DAG(dag_id="demo", start_date=datetime(2022, 1, 1), schedule="0 0 * * *") as dag:
     - By using this method, we will be have all tasks and bit shift operators to arrange tasks within the DAG.
     - All the general props of the DAG will come as arguments to the DAG which will be common for all the tasks of the DAG.

##### 2. Using Decorator DAG:
     @dag(
     schedule=None,
     start_date=pendulum.datetime(2021, 1, 1, tz="UTC"),
     catchup=False,
     tags=["example"],
     )
    def dag_function():

     - Using decorator @dag() with all the general props as arguments and creating a function below that.
     - And have all the tasks inside this function.
     - Call the tasks functions within the function.
     - Also the bit shifts inside this function.
     - And finally call the function.

##### 3. Directly instantiating the DAG class:
     dag = DAG('my_dag', default_args=default_args)
     - Create tasks separately using different approaches of creating the tasks.

#### TASK DEFINITION:
     The Next step is to define the tasks that the DAG is comprised of and in what order they should be executed.

##### WAYS OF DEFINING TASKS:

###### 1. Instatiating Opeartors:
     t1 = BashOperator(
        task_id="print_date",
        bash_command="date",
        )



### DIFFERENT TYPES OF GENERAL PROPS OF DAG:
     with DAG(
     "tutorial",
     # These args will get passed on to each operator
     # You can override them on a per-task basis during operator initialization
     default_args={
        "depends_on_past": False,
        "email": ["airflow@example.com"],
        "email_on_failure": False,
        "email_on_retry": False,
        "retries": 1,
        "retry_delay": timedelta(minutes=5),
        # 'queue': 'bash_queue',
        # 'pool': 'backfill',
        # 'priority_weight': 10,
        # 'end_date': datetime(2016, 1, 1),
        # 'wait_for_downstream': False,
        # 'sla': timedelta(hours=2),
        # 'execution_timeout': timedelta(seconds=300),
        # 'on_failure_callback': some_function, # or list of functions
        # 'on_success_callback': some_other_function, # or list of functions
        # 'on_retry_callback': another_function, # or list of functions
        # 'sla_miss_callback': yet_another_function, # or list of functions
        # 'trigger_rule': 'all_success'
     },
     description="A simple tutorial DAG",
     schedule=timedelta(days=1),
     start_date=datetime(2021, 1, 1),
     catchup=False,
     tags=["example"],
     ) as dag:

     -- The default args is common for all tasks and can be altered for each task separately.
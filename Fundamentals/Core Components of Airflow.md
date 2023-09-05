## 1. WebServer:
     It is a Flask Server  
     Is used to monitor our workflows in the UI.

## 2. Scheduler:
     It is used to schedule our Jobs at specific time.
     We can have multiple schedulers running at the same time and thus its fail safe.

## 3. Metadata Database:
     All Metadata related to connections, users, Airflow is stored in Metadata database.
     Any DB, which is compatible with SQLAlchemy is compatible with Airflow.
     Even MongoDB is compatibke with few limitations.

## 4. Executor:
     This defines how the Job is going to be executed by Airflow.

## 5. Worker:
     The executor defines , how the Job is to be executed and in which system.
     Whereas Worker is process or subprocess which gets created and where the tasks are executed.
     The task plan created by executors are sent to the worker nodes and the worker node start executing their tasks as processes or subprocesses.
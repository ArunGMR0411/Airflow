# Basic Commands

## DB Commands
> airflow db init
The Command used to initialize the Metadatabase used by Airflow.

> airflow db upgrade
This command is used to upgrade the metadatabase.

> airflow db reset
Use this with caution, this will erase everything in the Airflow system and will provide us with fresh system.


## Webserver Commands

> airflow webserver
This is used to start the webserver of the Airflow.


## Celery
> airflow celery worker
This commands, makes the current Node a celery worker node - and thus let celery use the node as workers for Airflow process.
Celery is an executor.

## DAGS
> airflow dags pause and airflow dags unpause

> airflow dags trigger
Used to trigger a DAG if we don't have access to the 

>airflow dags trigger -e <time>
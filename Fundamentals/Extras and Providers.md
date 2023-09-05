# Extras
     > By default, Airflow has its own set of core functionalities sunch as sending out mails when the Job fails, providing a local executor to execute the tasks.
     > In order to use some additional functionalities such as executing the tasks using celery executor - in that case we use the Extras.
     > That is by Extras we mean, we install all the necessary packages of celery and also its dependencies.
     > Now that the Celery package along with the dependencies required by Celery is installed - Airflow integrates with Celery and not have extended functionalities.

# Providers
     > Providers is more or less similar to Extras, whereas Providers is the tools that provides Airflow with the capablities to extend its functionality.
     > So if we consider connecting to Postgres system from Airflow, Postgres provider will provide us with the package to connect Airflow to postgres.

From this we could understand, Extras is packages provided by Providers for increased along with some extrernal dependency package.
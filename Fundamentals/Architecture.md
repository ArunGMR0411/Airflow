# Single Node Architecture  
All the core components of the Airflow are inside the same node.

## Metastore
    All the DAG details, Airflow details, Executor Nodes, Worker Nodes - All such details of Airflow are stored here and is accessed by Executor, Scheduler, Webserver as necessary.

## Webserver
    Webserver interacts with the metastore and helps us track everything that is needed in the form of User Interface using the WebApp where we can see all the DAGS and flow of the job, the logs, Users, their permissions.

## Scheduler
    Scheduler Job is to, whenever a User schedules a Job using the webserver or CLI, it updates the timing details in the metastore.
    To understand easily, Scheduler keeps track of timings of all the tasks that are being created in the Airflow and updates it in the Metastore.
    Then, it creates the TASK INSTANCE IMAGE and sends it to the executor's Queue. (Queue is part of the executor)

## Executor
    > Executor, based on tasks instance created and stored in the Queue will create a plan for the Workers to what exactly needs to be done and by which worker. In Simple terms, Executors will tell Workers what work/task to be taken and worked on by which Worker Node.
    > Another work of the executor is, post the completion of a task - it is its duty to update the metastore with the update status in the metastore.

# Worker
    > Worker Nodes Job is to fetch the tasks created by Scheduler in the Queue and work on them based on the suggestion by Executors.


> Continue to Core Concepts

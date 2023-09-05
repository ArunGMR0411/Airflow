# Life cycle of the tasks
     1. A Python file is created and placed in the Dags Directory - this file comprises of the Data Pipeline Skeleton.
     2. The File is parsed by both Webserver and Scheduler.
     3. Webserver gets updated every 30 seconds.
     4. Scheduler gets updated every 5 mins.
     5. Now, after 5 mins - Scheduler after parsing the Python file - Scheduler now creates a DagRun Object in the Metastore.
     6. DagRun status will be running in the metastore stating, the tasks in the Dag will run when the time comes.
     7. Now, the status of the task instance object will be NO STATUS.
     8. When the time provided for the task to run comes, the task instance object is created by the Scheduler and is pushed into the Metastore and now the status in Metastore is SCHEDULED.
     9. Then, the task instance object is sent to the Queue of Executors and now the status is QUEUED.
     10. Then the executor assigns the workers with their work for each tasks.
     11. The workers take their work based on executors suggestion and does the Job. Now, the status of the Task Instance Object is RUNNING.
     12. For now on, it is the work of the executor to update the metastore with status of the tasks either Success/Failed.
     13. Once all the tasks are updated by executors, the scheduler updates the DagRun Object with SUCCESS/FAILURE.
     14. The webserver now reads the Metastore and updates the UI accordingly.
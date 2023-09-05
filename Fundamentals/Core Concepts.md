# Core Concepts of Airflow

## DAGs
     > DAG is a Directed Acyclic Graph.
     > There should not be any loops.
     > This is the data pipeline of Airflow.
     > This comprises of multiple Tasks - Starting from T1 and going till nth task.
     > The same task should not be repeated in the flow of graph.

## Operator
     > Operator is an Object around the tasks of the DAG.
     > Each Operator that we have in our DAG is one of the tasks of the DAG.

## There are 3 types of Operators:
### Action Operators
     > Executing some actions in the Job.
### Transfer Operators
     > An Operator used for transfer of data from One process to another.
### Sensor Operators
     > An Operator that is used to look/wait for a particular action to happen and then triggers. Ex: When watching for Files in a directory.
### Set-upstream/Set-downstream Operators also called Shift Operators:
     > This Operator is used to define the dependencies of the tasks.
     > Denoted by >> or <<

## Tasks
     > Task is an instance of the Operator.
     > When a task is ready to scheduled, it gets converted into task instance and pushed into the queue of Executors.
     
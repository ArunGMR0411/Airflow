## What is Airflow
    Open Source Platform.
    Used to programatically author, schedule and monitor workflows/pipelines.
    Used to execute Dynamic Pipelines in the right order, in right time.

## What Airflow does ?
    Trigger a Spark Job, Python Job or any Job can be triggered using Airflow.
    Warns us if there is any failure in the Pipeline.

## Features:
    Written in Python thus it can doanything that Python does.
    This is highly Interactive - User Interface, Airflow CLI, Astro CLI, Rest API (Connecting to Airflow using our own WebApp)

## What is not a Airflow ?
    It is an orchestrator and not a data processing framework - thus we should use it Spark to process data and use Airflow to pipeline the Spark jobs.
    Not a Streaming Process - Don't keep executing the Airflow process in Loops.
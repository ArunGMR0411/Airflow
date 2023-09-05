# Main reasons to use Airflow

## 1. Failure of Jobs:
Lets consider we have multiple tasks throughout a pipeline, and we need to have proper exceptionhandling across each tasks and also, if we are using cron or Autosys - we should catch the error from Spark or python job and send it to cron or Autosys and log it whereas using Airflow makes this error handling easier.

## 2. Monitor our tasks using UI:
Like in Autosys, Airflow also has proper UI for viewing the pipeline and also shows us clear image representations of tasks better than Autosys.
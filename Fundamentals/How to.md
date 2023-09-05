# How to initialize the Airflow  
## 1. Install Astronomer CLI  
     First, the AstromerCLI is downloaded and installed in the system, then set the environment variables.

## 2. First Command:  
     astro dev init  

This initializes the Airflow system in our server with necessary default files needed for executing the starting the Airflow system which comprises of containers of Schedulers, Trigerrers, Webservers and Database Systems.

## 3. Second Command:
     astro dev start  

This starts the necessary containers mentioned in the above point and we now have Orchestration ready to be worked on.

## 4. Check running Airflow processes
     astro dev ps

This will show us the containers/processes which have started as part of the 3rd command.
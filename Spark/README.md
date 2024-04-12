# pySpark Docker Deployment

This repository contains a Docker Compose configuration for deploying Spark and Jupyter using Docker.

## Contents

- `docker-compose.yml`: Docker Compose configuration file for deploying Spark and Jupyter.

This docker-compose contains the following services:

- `Spark master`: Coordinates Spark applications, manages resources, and schedules tasks across worker nodes in the Spark cluster.
- `Spark worker`: Executes tasks assigned by the Spark master, processing data and performing computations within the Spark cluster.
- `Jupyter`: It´s a notebook where you can use spark (Java is already instaled)

## Deployment

To deploy Spark and Jupyter using Docker, follow these steps:

1. Make sure you have Docker installed on your system and Docker Desktop is open.

2. Navigate to the directory containing the `docker-compose.yml` file.

3. Open a terminal and run the following command to start Spark and Jupyter services:
   
   ```bash
   docker-compose up -d
   ```

4. *Your Jupyter notebook* at [http://localhost:8888/](http://localhost:8888/).
   
5. You can access the notebook by entering the token, or you can log in by entering the token and setting a new password:
    * Token: GFTOKEN
  
6. *Spark-ui* at [http://localhost:9090/](http://localhost:9090/).
  
7. Once you have finished using NiFi turn down the continers.
    ```bash
    docker-compose down
    ```


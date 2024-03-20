# Jupyter notebook Docker Deployment

This repository contains a Docker Compose configuration for deploying Jupyter notebook services using Docker Compose.

## Contents

- `docker-compose.yml`: Docker Compose file to deploy a Jupyter notebook service.

This docker-compose contains the following services:

- **jupyter**: Jupyter is an open-source web application that allows you to create and share documents that contain live code, equations, visualizations, and narrative text. It supports various programming languages, such as Python or R. 

## Deployment

1. Make sure you have Docker installed on your system and open Docker Desktop.

2. Navigate to the directory containing the `docker-compose.yml` file.

3. Open a terminal and run the following command:
   ```bash
   docker-compose up -d
   ```

4. *Your Jupyter notebook* at [http://localhost:8888/](http://localhost:8888/).

5. You can access the notebook by entering the token, or you can log in by entering the token and setting a new password:
    * Token: GFTOKEN

6. Once you have finished using NiFi turn down the continers.
    ```bash
    docker-compose down
    ```
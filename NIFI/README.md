# NiFi Docker Deployment

This folder contains a Docker Compose configuration for deploying NiFi using Docker Compose.

## Contents

- `docker-compose.yml`: Docker Compose configuration file for deploying NiFi.

## Deployment

To deploy NiFi using Docker, follow these steps:

1. Make sure you have Docker installed on your system and open Docker Desktop.

2. Navigate to the directory containing the `docker-compose.yml` file.

3. Open a terminal and run the following command to start NiFi:
   ```bash
   docker-compose up -d
4. NiFi will be accesible throught your web broser at [https://localhost:8443/nifi/](https://localhost:8443/nifi/)

5. Credentials:
    * Username: admin
    * Password: ctsBtRBKHRAx69EqUghvvgEvjnaLjFEB

6. Once you have finished using NiFi turn down the continers.
    ```bash
    docker-compose down

Note: The volume ./template:/opt/nifi/nifi-current/conf/templates/ will charge in NiFi all the templates that you have in the folder ./template

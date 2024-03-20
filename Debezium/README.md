# Debezium Docker Compose Deployment

# NOT TESTED. IN PORGRESS...

This repository contains several `docker-compose.yml` files that allow you to deploy different configurations of Debezium and its additional components using Docker Compose.

## Contents

- `docker-compose.yml`: Docker Compose file to deploy debezium, kafka, Postgres and pgAdmin services.

This docker-compose contains the following services:

- **debezium**: Debezium is a CDC (Change Data Capture) distributed platform that captures events from databases and sends them to a topic (Kafka), allowing real-time data processing.
- **kafka**: [here](/Kafka/README.md).
- **zookeeper**: [here](/Kafka/README.md).
- **postgres**: [here](/PostgreSQL/README.md).
- **pgadmin**: [here](/PostgreSQL/README.md).

Debezium is normally used with kafka, but that is not mandatory.

## Deployment

1. Make sure you have Docker installed on your system and open Docker Desktop.

2.  Navigate to the directory containing the `docker-compose.yml` file.

3. Open a terminal and run the following command:
   ```bash
   docker-compose up -d
   ```

4. *pgadmin* at [http://localhost:5050](http://localhost:5050).

5. Credentials:
    * Username: pgadmin4@pgadmin.org
    * Password: pepe

6. Once you have finished using NiFi turn down the continers.
    ```bash
    docker-compose down
    ```
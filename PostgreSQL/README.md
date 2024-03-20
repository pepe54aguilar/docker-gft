# Postgres and pgAdmin Docker Compose Deployment

This repository contains a Docker Compose configuration for deploying Postgres and pgAdmin services using Docker Compose.

## Contents

- `docker-compose.yml`: Docker Compose file to deploy Postgres and pgAdmin services.

This docker-compose contains the following services:

- **postgres**: Postgres is a powerful, open-source *relational database management* system.
- **pgadmin**: pgAdmin is a web-based *administration tool* for managing *PostgreSQL* databases. It provides a user-friendly *interface* for database administration tasks such as creating and managing databases, tables, and queries.

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
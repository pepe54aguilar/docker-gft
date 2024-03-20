# MongoDB and MongoDB express Docker MongoDB Deployment

This repository contains a Docker Compose configuration for deploying MongoDB and MongoDB express services using Docker Compose.

## Contents

- `docker-compose.yml`: Docker Compose file to deploy MongoDB and MongoDB express services.

This docker-compose contains the following services:

- **mongodb**: MongoDB is a flexible, scalable, NoSQL document database. It is designed to store data in JSON-like documents with dynamic schemas.
- **mongodb-express**: MongoDB express is a *GUI (Graphical User Interface)* for MongoDB. It provides an intuitive interface for exploring and interacting with MongoDB databases. 

## Deployment

1. Make sure you have Docker installed on your system and open Docker Desktop.

2. Navigate to the directory containing the `docker-compose.yml` file.

3. Open a terminal and run the following command:
   ```bash
   docker-compose up -d
   ```

4. *mongo-express* at [http://localhost:8081/](http://localhost:8081/).

5. Credentials:
    * Username: admin
    * Password: pass

6. Once you have finished using NiFi turn down the continers.
    ```bash
    docker-compose down
    ```
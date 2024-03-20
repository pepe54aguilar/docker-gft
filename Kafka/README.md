# Docker Compose for Kafka and Additional Components

This repository contains several `docker-compose.yml` files that allow you to deploy different configurations of Kafka and its additional components using Docker Compose.

## Contents

- `kafka_basic/`: Folder containing a `docker-compose.yml` file to deploy Kafka and Zookeeper.
- `kafka-ksql/`: Folder containing a `docker-compose.yml` file to deploy Kafka, Zookeeper, KSQL-server, ksql-cli and control-center.
- `kafka-advanced/`: Folder containing a `docker-compose.yml` file to deploy Kafka, Zookeeper, KSQL-server, control Center, kafka-ui, kafka-connect, schema-registry, postgres and pgadmin.

### kafka_basic

This folder contains the Kafka and Zookeeper services.
- **kafka**: Kafka service.
- **Zookeeper**: Service responsible for controlling Kafka brokers. Zookeeper must be running for kafka to work.

### kafka_ksql

This folder contains `kafka_basic` + ksql-server, ksql-cli and control-center services.
- **ksql-server**: KSQL is a streaming query engine that enables real-time analysis of data streams in Kafka using standard *SQL queries*.
- **ksql-cli**: KSQL command-line interface (CLI) provides an interactive *shell* for executing KSQL queries and managing KSQL server instances.
- **control-center**: Confluent Control Center is a *graphical user interface* (GUI) for managing and monitoring Kafka clusters. It offers intuitive dashboards for monitoring performance, managing connectors, running KSQL queries, configuring alerts, and more.

### kafka_advanced
This folder contains `kafka-ksql` + kafka_ui, kafka-connect, schema-registry services.
- **kafka-ui**: Kafka UI is a *web-based user interface* for monitoring and managing Kafka clusters. It provides features such as topic management, consumer group monitoring, and message browsing.
- **kafka-connect**: Kafka Connect is a framework for *connecting* Kafka with *external systems* such as databases, storage systems, and messaging systems.
- **schema-registry**: Schema Registry is a service that *manages Avro schemas* for Kafka topics. It provides a centralized repository for storing and retrieving schemas, ensuring compatibility and consistency in data serialization and deserialization.

It also contains postgres and pgadmin services, whereas they doesn't depends on kafka.
- **postgres**: Postgres is a powerful, open-source *relational database management* system.
- **pgadmin**: pgAdmin is a web-based *administration tool* for managing *PostgreSQL* databases. It provides a user-friendly *interface* for database administration tasks such as creating and managing databases, tables, and queries.

## Deployment

1. Make sure you have Docker installed on your system and open Docker Desktop.

2.  Navigate to the directory containing the `docker-compose.yml` file.

3. Open a terminal and run the following command:
   ```bash
   docker-compose up -d
4. - *control-center* at [http://localhost:9021](http://localhost:9021).
    - *kafka-ui* at [http://localhost:8080](http://localhost:8080).
    - *pgadmin* at [http://localhost:5050](http://localhost:5050).

5. Credentials for pgadmin:
    - user: pgadmin4@pgadmin.org
    - password: admin

6. Once you have finished using NiFi turn down the continers.
    ```bash
    docker-compose down
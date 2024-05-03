# Postgres SQL Docker Compose Setup [![JavaScript](https://skillicons.dev/icons?i=docker)](https://skillicons.dev)

This repository contains a Docker Compose configuration for setting up a PostgreSQL database server using Docker.

## Prerequisites

Before you begin, ensure you have Docker and Docker Compose installed on your system.

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Usage

1. Clone this repository to your local machine:

    ```
    git clone https://github.com/your-username/postgres-docker-compose.git
    ```

2. Navigate to the cloned directory:

    ```
    cd postgres-docker-compose
    ```

3. Start the PostgreSQL server by running:

    ```
    docker-compose up -d
    ```

   This command will create and start a PostgreSQL container named `my_postgres_db` using the settings specified in `docker-compose.yml`. The database will be accessible on port 5432.

4. You can now connect to the PostgreSQL database using your preferred client tool (e.g., psql, pgAdmin) using the following connection details:

    - **Host:** localhost
    - **Port:** 5432
    - **Username:** myuser
    - **Password:** mypassword
    - **Database:** mydatabase

5. To stop the PostgreSQL server, run:

    ```
    docker-compose down
    ```

   This command will stop and remove the PostgreSQL container. Your data will persist in the `./data` directory on your host machine.

## Configuration

You can customize the PostgreSQL server settings by modifying the `docker-compose.yml` file. Here are some key configurations you might want to change:

- `POSTGRES_USER`: The username for the PostgreSQL user.
- `POSTGRES_PASSWORD`: The password for the PostgreSQL user.
- `POSTGRES_DB`: The name of the default database to be created.
- Port mappings: You can change the port mappings if you want to use a different host port for accessing the PostgreSQL server.

## Persistence

The PostgreSQL data is persisted on your host machine in the `./data` directory. This ensures that your database data survives container restarts and removals.


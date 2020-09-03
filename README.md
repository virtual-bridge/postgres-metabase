# Metabase with a PostgresSQL Backend

Metabase is an open-source java-based software that enables users to analyse data from a range of data sources including relational databases (e.g. PostgreSQL, MySQL etc.), NoSQL databases, Google Analytics and more. 

Metabase can be run using the default H2 database backend but recommend using PostgreSQL for this and is easy enough to setup in the same compose file (or you could change the config to point at an existing Postgres cluster if you have one)


## Requirements

- You will need a docker host with compose installed (or locally with Docker Desktop)
- Clone this repository

## Configuration
- Copy the .env.sample to .env and update the values as required with your desired credentials for the postgres and metabase database credentials

## Usage

```bash
docker-compose up -d
```

Will load the environment up as a daemon. 

You can then hit http://yourhost:3001 in your browser. Run through the setup to create a local metabase admin.

As part of the setup you can choose to add a database server 

> Note that you can change the ports in the config file as required if you do not want to access on 3001, i.e 443/80 etc
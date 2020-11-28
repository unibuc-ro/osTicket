# osTicket - custom version

This is a customized version of osTicket, adapted for the University of Bucharest's needs.

The original `README` can be found [here](README.original.md).

## Running with Docker

You can run a local instance of osTicket using [Docker](https://www.docker.com/) and [docker-compose](https://docs.docker.com/compose/).

Start the services using:

```sh
docker-compose up
```

This starts a container with an Apache server and a container with a MySQL database.
You can access the local instance at `http://localhost:8080`.

### Initial database setup

If it's the first time you're running it, or after you've deleted the database,
you should copy the `include/ost-sampleconfig.php` file to `docker/ost-config.php`
to run the installer.

Make sure you specify the following database settings:

- MySQL Hostname: `mysql`
- MySQL Database: `osticket`
- MySQL Username: `osticket`
- MySQL Password: `osticket_pwd`

### phpMyAdmin

For exploring the database, you can access the phpMyAdmin container at `http://localhost:8000`.

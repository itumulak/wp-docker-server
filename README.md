# WP Docker server

This is docker stack that let's you spin up WordPress server.

## Prerequisites

- Docker

## Stack

- WordPress
- MySQL
- PHPMyAdmin

## Getting started

Update `.env` to change container name, ports, credentials, etc.

Run `docker-compose.yml`.

```sh
docker compose up -d
```

Go to https://localhost:8080 (or what port you have define in .env) and complete the wordpress installation.

A `wordpress_data` folder should exists now. This is where WordPress instance will reside.

## FAQs

**Q:** I got a **Permission Denied** when adding new files in `wordpress_data` folder.

**A:** Set the folder permission.

> [!WARNING]
> This is not advisable in production server.

```sh
chown -R 777 ./wordpress_data
```

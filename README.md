# Demo Wordpress Site (Docker)

A portable wordpress site. Uses NGINX and MariaDB. [Take a look at the demo here](http://wordpress.orangeburrito.com/)

## Commands
Running
```sh
# Dev
docker compose up -d

## Prod
docker compose -f compose.yml -f compose.prod.yml up -d
```

Stopping
``` sh
# Stop
docker compose stop

# Remove all containers
docker compose down -v
```

Editing Config files 
```sh
# After editing nginx.conf
docker compose restart nginx

# After editing php.ini
docker compose restart wordpress
```

## Development URLs
```sh
# Wordpress
http://localhost:8080

# Adminer
http://localhost:8081
```
(Adminer username and password uses `SQL_USER` / `SQL_PASSWORD` in `.env`)

## ENV Variables

Sample `.env` file
```
SQL_ROOT_PASSWORD=rootpassword
SQL_USER=username
SQL_PASSWORD=password
SITE_DOMAIN=mydomain.com
SITE_ADMIN_EMAIL=admin@mydomain.com
```

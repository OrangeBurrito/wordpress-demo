# Demo Wordpress Site (Docker)

A portable wordpress site. Uses NGINX and MariaDB.

## Commands
Run in dev
`docker compose up -d`

Run in prod
`docker compose -f compose.yml -f compose.prod.yml up -d`

Stop
`docker compose stop`

Remove all
`docker compose down -v`

After editing `nginx.conf`
`docker compose restart nginx`

After editing `php.ini`
`docker compose restart wordpress`

## URLs
WP runs at
`http://localhost:8080`

Adminer
`http://localhost:8081`
(server `db`, user and password from `SQL_USER` / `SQL_PASSWORD` in `.env`)

## ENV Variables

Sample `.env` file
```
SQL_ROOT_PASSWORD=rootpassword
SQL_USER=username
SQL_PASSWORD=password
SITE_DOMAIN=mydomain.com
SITE_ADMIN_EMAIL=admin@mydomain.com
```

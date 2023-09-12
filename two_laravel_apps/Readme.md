# Compose Toolbox

## Two identical Laravel Projects

In my work, I have to mantain a system consisting in two Laravel 8 projects, running in PHP 7.4 in production. One is the Portal that acts as a public front-end, and the other one as a back-end (which has a database and an API for the Portal) and a front-end for the administrative people at the company. To develop locally, I made this docker-compose file to serve both Laravel projects at the same time.

### Usage

Rename the folders and database credentials of this file, then just run:

`docker-compose up portal`

This will build both Laravel containers using the same Dockerfile in this folder. The dump of the database should be in the same folder of this file, named as `init.sql`. It does not use Artisan Migrations.
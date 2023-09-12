# Compose toolbox

## Composer for PHP 7.4 everywhere runner

This is a small helper that creates a container that lets you run `composer` in your project's folder, without installing it and bloating your O.S. Note that we need to build a container due to the projects being bound to PHP 7.4, and all composer docker images are based on PHP 8 and onwards.

This is compatible with the Dockerfile found in the `two_laravel_apps` folder.

### Usage

Just run:

`docker-compose run --rm composer [args]`

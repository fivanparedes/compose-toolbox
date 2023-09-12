# make a dockerfile for this laravel project
FROM php:7.4-fpm-alpine

# install php extensions
RUN docker-php-ext-install pdo pdo_mysql

# install composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# set working directory
WORKDIR /var/www/html

# copy source code
COPY . /var/www/html

# install dependencies
RUN composer install

# copy .env file
COPY .env.example .env

# generate key
RUN php artisan key:generate

# expose port 8000 and start php-fpm server
EXPOSE 8000
CMD ["php-fpm"]



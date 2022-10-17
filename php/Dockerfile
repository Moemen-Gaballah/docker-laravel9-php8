FROM php:8.0-apache

RUN apt-get update && apt-get install -y  apt-transport-https \
            curl \
            g++ \
            libicu-dev \
            libpq-dev \
            libzip-dev \
            zip \
            zlib1g-dev \
            curl \
            wget \
            vim \
            git \
        && docker-php-ext-install \
            intl \
            opcache \
            pdo \
            pdo_mysql \
            pdo_pgsql \
            pgsql

WORKDIR /var/www/laravel_docker

RUN chown -R www-data:www-data /var/www

RUN chmod -R 777 ./

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
FROM php:8.0-fpm

RUN apt-get update \
    && apt-get install -y zlib1g-dev libzip-dev zip unzip mariadb-client \
    && docker-php-ext-install zip pdo_mysql

RUN curl -sL https://deb.nodesource.com/setup_12.x | bash - \ 
    && apt-get update \
    && apt-get install -y nodejs

COPY --from=composer /usr/bin/composer /usr/bin/composer

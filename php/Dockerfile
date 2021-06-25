FROM php:7.4.20-fpm

RUN pecl install redis-5.1.1 \
    && docker-php-ext-enable redis \
    && docker-php-ext-install pdo_mysql
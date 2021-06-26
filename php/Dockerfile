FROM php:7.4.20-fpm

RUN pecl install redis-5.1.1 \
    && docker-php-ext-enable redis \
    && docker-php-ext-install pdo_mysql

RUN curl -sS https://getcomposer.org/installer | php \
    && mv composer.phar /usr/local/bin/composer \
    && composer config -g repo.packagist composer https://mirrors.aliyun.com/composer/

WORKDIR /var/www    
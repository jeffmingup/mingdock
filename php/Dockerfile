FROM php:7.4.20-fpm

RUN apt-get update && apt-get install -y git unzip vim\
    && pecl install redis-5.1.1 \
    && docker-php-ext-enable redis  \
    && docker-php-ext-install pdo_mysql \
    && docker-php-ext-install bcmath 

ADD https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/

RUN chmod +x /usr/local/bin/install-php-extensions && sync && \
    install-php-extensions yaml mongodb

RUN curl -sS https://getcomposer.org/installer | php \
    && mv composer.phar /usr/local/bin/composer \
    && composer config -g repo.packagist composer https://mirrors.aliyun.com/composer/

COPY .ssh/ /root/.ssh/
WORKDIR /var/www    
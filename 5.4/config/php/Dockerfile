FROM php:5.4-apache

COPY ./php.ini /usr/local/etc/php/

COPY ./apache2.conf /etc/apache2/
COPY ./sites/*.conf /etc/apache2/site-avaliable/
COPY ./conf/*.conf  etc/apache2/conf-avaliable/

RUN apt-get update \
    && apt-get install -y libpq-dev \
    && docker-php-ext-install pdo_mysql pdo_pgsql mysqli mbstring

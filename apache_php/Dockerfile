FROM php:7-apache
MAINTAINER mcarballodd <test@gmail.com>

COPY php.ini /usr/local/etc/php/
COPY index.php /var/www/html

RUN apt-get update \
  && apt-get install -y libfreetype6-dev libjpeg62-turbo-dev libpng12-dev libmcrypt-dev \
  && docker-php-ext-install pdo_mysql mysqli mbstring gd iconv mcrypt

EXPOSE 80

WORKDIR /var/www/html

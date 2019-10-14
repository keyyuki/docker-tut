FROM php:7.2.10-fpm

#COPY php.ini /usr/local/etc/php/php.ini
RUN cp /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini
# Install common lib, libmcrypt-dev need for install "mcrypt" ext
RUN apt-get update \
    && apt-get install -y nano unzip curl htop libmcrypt-dev

RUN docker-php-ext-install pdo pdo_mysql calendar zip gd

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /opt/www/myfirstapp
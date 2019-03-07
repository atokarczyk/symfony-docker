FROM php:7.2-apache-stretch
WORKDIR /var/www
RUN rm -rf /var/www/html && a2enmod rewrite && DEBIAN_FRONTEND=noninteractive apt-get -y update && apt-get -y install zlib1g-dev zip curl 
RUN docker-php-ext-install zip
COPY --from=composer /usr/bin/composer /usr/bin/composer

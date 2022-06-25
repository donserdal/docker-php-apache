FROM php:7.4.30-apache
LABEL maintainer="Serdal Ozkan <Donserdal@hotmail.com>"

RUN apt-get update -y && apt-get install -y libpng-dev libpq-dev libzip-dev libonig-dev
RUN docker-php-ext-install mbstring 
RUN docker-php-ext-install pdo_mysql 
RUN docker-php-ext-install zip 
RUN docker-php-ext-install gd 
#RUN docker-php-ext-install pdo  
#RUN docker-php-ext-install zlib 
#RUN docker-php-ext-install json 
#RUN docker-php-ext-install simplexml 
#RUN docker-php-ext-install curl 
#RUN docker-php-ext-install imagick 
# RUN composer install

RUN a2enmod rewrite

RUN apt-get update && apt-get install -y \
    libmagickwand-dev --no-install-recommends \
    && pecl install imagick \
	&& docker-php-ext-enable imagick


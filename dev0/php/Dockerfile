FROM php:5.6.40-fpm
WORKDIR /application

ENV ACCEPT_EULA=Y

# ADD User
RUN useradd -u 1000 www

# Fix debconf warnings upon build
ARG DEBIAN_FRONTEND=noninteractive

# MySQLi 
RUN docker-php-ext-install mysqli 
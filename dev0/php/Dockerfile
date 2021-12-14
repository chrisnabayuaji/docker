FROM php:5.6.40-fpm
WORKDIR /application

ENV ACCEPT_EULA=Y

# ADD User
RUN useradd -u 1000 www

# Fix debconf warnings upon build
ARG DEBIAN_FRONTEND=noninteractive

# MySQLi 
RUN docker-php-ext-install mysqli 

# Imagick
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        libmagickwand-dev \
    && rm -rf /var/lib/apt/lists/*

RUN pecl install imagick-3.4.1 \
    && docker-php-ext-enable imagick
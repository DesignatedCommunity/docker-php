FROM php:7.1-fpm
RUN apt-get update && apt-get install -y \
        libmcrypt-dev \
        libxml2-dev \
    && docker-php-ext-install -j$(nproc) iconv mcrypt mysqli soap


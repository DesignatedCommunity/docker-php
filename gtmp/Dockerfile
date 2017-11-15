FROM php:7.1-fpm
RUN apt-get update && apt-get install -y \
        libxml2-dev \
    && docker-php-ext-install -j$(nproc) soap

FROM php:7.1-fpm-alpine
RUN apk update && apk add \
        # nproc
        coreutils \
        # php-mcrypt
        libmcrypt-dev \
        # php xml
        libxml2 \
    && docker-php-ext-install -j$(nproc) mysqli mbstring xml

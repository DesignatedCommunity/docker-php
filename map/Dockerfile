FROM php:5.6-fpm-alpine
RUN apk update && apk add \
        # nproc
        coreutils \
        # php-mcrypt
        libmcrypt-dev \
        # php-gd
        libjpeg-turbo-dev \
        # php-gd
        libpng-dev \
        # php-gd
        freetype-dev \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install -j$(nproc) iconv mcrypt mysql mysqli pdo_mysql gd

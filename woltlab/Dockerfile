FROM php:7.2-fpm-alpine
RUN apk add --no-cache \
    # nproc
    coreutils \
    # php-gd
    libjpeg-turbo-dev \
    # php-gd
    libpng-dev \
    # php-gd
    freetype-dev \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install -j$(nproc) pdo_mysql gd

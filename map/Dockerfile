FROM php:5.6-fpm-alpine
RUN apk update && apk add \
        # nproc
        coreutils \
    && docker-php-ext-install -j$(nproc) mysql mysqli pdo_mysql

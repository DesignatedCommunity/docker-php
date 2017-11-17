FROM php:7.1-fpm-alpine
RUN apk update && apk add \
        # nproc
        coreutils \
        # php-soap
        libxml2-dev \
    && docker-php-ext-install -j$(nproc) soap

FROM php:7.2-fpm-alpine
RUN apk add --no-cache \
        # nproc
        coreutils \
        # php-soap
        libxml2-dev \
    && docker-php-ext-install -j$(nproc) mysqli soap
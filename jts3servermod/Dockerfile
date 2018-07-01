FROM php:7.2-fpm-alpine
RUN apk add --no-cache \
        # nproc
        coreutils \
    && docker-php-ext-install -j$(nproc) mysqli

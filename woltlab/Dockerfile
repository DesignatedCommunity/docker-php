FROM php:7.2-fpm-alpine
ENV PHPREDIS_VERSION 4.0.2
RUN apk add --no-cache \
    # php-gd
    libjpeg-turbo-dev \
    libpng-dev \
    freetype-dev \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    # php-redis
    && mkdir -p /usr/src/php/ext/redis \
    && curl -L https://github.com/phpredis/phpredis/archive/$PHPREDIS_VERSION.tar.gz | tar xvz -C /usr/src/php/ext/redis --strip 1 \
    && echo 'redis' >> /usr/src/php-available-exts \
    # install and clean
    && docker-php-ext-install pdo_mysql gd redis
FROM php:8.3-cli

RUN apt-get update && apt-get install -y \
        libcurl4-openssl-dev \
        libbrotli-dev \
        libc-ares-dev \
        libssl-dev \
        apt-utils \
        procps \
        curl \
        zip

RUN docker-php-ext-configure pcntl --enable-pcntl
RUN docker-php-ext-install pdo pdo_mysql pcntl opcache

RUN pecl install xdebug \
        redis

RUN pecl install -D 'enable-sockets="no" enable-openssl="yes" enable-http2="yes" enable-mysqlnd="yes" enable-swoole-json="no" enable-swoole-curl="yes" enable-cares="yes"' swoole

RUN docker-php-ext-enable xdebug \
        redis \ 
        swoole

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
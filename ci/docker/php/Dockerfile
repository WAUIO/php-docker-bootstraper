ARG PHP_VERSION=7.4

FROM php:${PHP_VERSION}-fpm
RUN apt-get update && apt-get install -y \
    libfreetype-dev \
    libjpeg62-turbo-dev \
    libpng-dev \
    ca-certificates \
    curl \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install -j$(nproc) gd \
    && docker-php-ext-install -j$(nproc) mysqli pdo pdo_mysql

EXPOSE 9000
CMD ["php-fpm"]
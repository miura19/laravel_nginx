FROM php:8.2.8-fpm-alpine3.18

COPY --from=composer /usr/bin/composer /usr/bin/composer

# RUN docker-php-ext-install pdo_mysql
# RUN curl -sL https://deb.nodesource.com/setup_16.x | bash -
# RUN apt-get install -y nodejs
RUN apk add --no-cache curl \
    && apk add --no-cache nodejs npm \
    && docker-php-ext-install pdo_mysql

# Node.jsをAlpine Linux向けにインストール
RUN apk add --no-cache nodejs-current npm
EXPOSE 5173
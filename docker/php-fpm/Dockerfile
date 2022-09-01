#Pull da imagem do php-fpm
FROM php:8.1.8-fpm-alpine

#Pasta raiz do projeto
WORKDIR "/var/www/colaboradores-farmarcas"

ARG DEBIAN_FRONTEND=noninteractive

#Adiciona mais algumas dependências
RUN apk add --no-cache openssl pcre-dev libtool \
bash nodejs npm postgresql-dev \
libxml2-dev

#Adiciona as extensões do php
RUN docker-php-ext-install bcmath pdo pdo_pgsql soap pcntl exif

#Adiciona o composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

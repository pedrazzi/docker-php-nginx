FROM php:8.1.0-fpm

ARG NODE_VERSION=16
ARG user=pedrazzi
ARG uid=1000

LABEL maintainer="Fabio Pedrazzi <pedrazzi@hotmail.com>"

# Seleciona a área de trabalho
WORKDIR /var/www

# Instala as dependências do php
RUN apt-get update && apt-get install -y
RUN apt-get install --fix-missing -y libpq-dev
RUN apt-get install --no-install-recommends -y libpq-dev
RUN apt-get install -y libxml2-dev libbz2-dev zlib1g-dev
RUN apt-get -y install curl exif ftp
RUN docker-php-ext-enable bcmath

# bcmath gd
# Instala última versão do composer
# COPY --from=composer:latest /usr/bin/composer /usr/bin/composer


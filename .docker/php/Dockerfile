FROM php:8.3-fpm

# Instala extensões necessárias para MySQL e outras ferramentas de estudo
RUN apt-get update && apt-get install -y \
    libpng-dev \
    libonig-dev \
    libxml2-dev \
    zip \
    unzip \
    curl

# Instala extensões do PHP (PDO MySQL é essencial para seus desafios)
RUN docker-php-ext-install pdo_mysql mbstring exif pcntl bcmath gd

WORKDIR /var/www/html

EXPOSE 9000

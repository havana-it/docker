FROM php:7.0-fpm

LABEL author="Yann Blacher for Havana IT & APPS" \
      description="PHP-FPM Image enriched with basic php extensions and vim" \
      license="MIT"

RUN apt-get update && apt-get install -y git libcurl4-gnutls-dev zlib1g-dev libicu-dev g++ libxml2-dev libpq-dev vim \
 && docker-php-ext-install pdo pdo_mysql intl curl json opcache xml bcmath \
   && apt-get autoremove && apt-get autoclean \
   && rm -rf /var/lib/apt/lists/*

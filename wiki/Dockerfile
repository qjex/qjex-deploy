FROM php:5.6-apache
MAINTAINER Andrew QjeX <theqjex@gmail.com>

RUN set -x; \
    apt-get update \
    && apt-get install -y --no-install-recommends \
        g++ \
        libicu52 \
        libicu-dev \
    && pecl install intl \
    && echo extension=intl.so >> /usr/local/etc/php/conf.d/ext-intl.ini \
    && apt-get purge -y --auto-remove g++ libicu-dev \
    && rm -rf /var/lib/apt/lists/*

RUN docker-php-ext-install mysqli opcache mbstring

RUN set -x; \
    apt-get update \
    && apt-get install -y --no-install-recommends imagemagick \
    && rm -rf /var/lib/apt/lists/*

RUN a2enmod rewrite

COPY apache/wiki.conf /etc/apache2/
RUN echo Include /etc/apache2/wiki.conf >> /etc/apache2/apache2.conf

CMD ["apache2-foreground"]


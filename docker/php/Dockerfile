FROM php:7.3-apache

RUN apt-get -y update

# Install mysqli extension
RUN docker-php-ext-install mysqli

# Install intl extension
RUN apt-get install -y libicu-dev \
    && docker-php-ext-configure intl \
    && docker-php-ext-install intl

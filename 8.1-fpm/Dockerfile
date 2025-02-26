FROM php:8.1-fpm

RUN apt-get update \
	&& apt-get dist-upgrade -y \
	# dependencies
	&& apt-get update && apt-get install -y \
        apt-transport-https \
        ca-certificates \
        unzip \
        libpq-dev \
        libmcrypt-dev \
        curl \
        libpng-dev \
        libjpeg-dev \
        zlib1g-dev \
        cron \
        libldap2-dev \
        libssl-dev \
        ldap-utils \
        nano \
        libzip-dev \
        zip \
        supervisor \
	# cleanup
	&& apt-get clean -y && apt-get autoclean -y && apt-get autoremove -y \
	&& rm -rf /var/lib/apt/lists/* /var/lib/log/* /tmp/* /var/tmp/*

RUN docker-php-ext-install gd
RUN docker-php-ext-install zip
RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-configure pgsql -with-pgsql=/usr/local/pgsql \
    && docker-php-ext-install pgsql pdo_pgsql
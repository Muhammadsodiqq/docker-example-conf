FROM php:7.4-fpm
ADD https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/
RUN apt-get update && apt-get install -y
RUN chmod +x /usr/local/bin/install-php-extensions && \
    install-php-extensions mcrypt gd pgsql pdo_mysql pdo_pgsql calendar zip exif ffi gettext intl mysqli opcache pcntl shmop sockets sysvmsg sysvsem sysvshm xsl


# COPY ./www.conf /usr/local/etc/php-fpm.d/www.conf
# RUN mv "$PHP_INI_DIR/php.ini-production" "$PHP_INI_DIR/php.ini"
# COPY ./php.ini "$PHP_INI_DIR/"
WORKDIR /var/www
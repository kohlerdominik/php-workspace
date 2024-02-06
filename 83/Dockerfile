FROM php:8.3-cli

RUN apt-get update \
## Install Tools from the package manager
  && apt-get install -y  git curl nano coreutils iputils-ping libzip-dev \
## Install PHP extensions from PECL
    && pecl install xdebug \
    && docker-php-ext-enable xdebug \
## Install PHP extensions via docker-php-ext
    && docker-php-ext-install zip
  
COPY --from=composer /usr/bin/composer /usr/bin/composer

COPY ./conf.d/ $PHP_INI_DIR/conf.d/

ENV PHP_IDE_CONFIG=serverName=docker.local
WORKDIR /app
ENTRYPOINT [ "sh", "-c"]
CMD ["/bin/bash"]

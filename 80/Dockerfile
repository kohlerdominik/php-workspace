FROM php:8.0-cli

RUN apt-get update \
## Install Tools from the package manager
  && apt-get install -y  git curl nano coreutils iputils-ping libzip-dev \
## Install PHP extensions from PECL
    && pecl install xdebug \
    && docker-php-ext-enable xdebug \
## Install PHP extensions via docker-php-ext
    && docker-php-ext-install zip

  
COPY --from=composer /usr/bin/composer /usr/bin/composer

WORKDIR /app
ENTRYPOINT [ "sh", "-c"]
CMD ["/bin/bash"]
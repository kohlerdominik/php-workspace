FROM php:7.4-cli

RUN apt-get update \
## Install PHP extensions from PECL
    && pecl install xdebug \
    && docker-php-ext-enable xdebug \
## Install Tools from the package manager
    && apt-get install -y  git curl nano coreutils iputils-ping

COPY --from=composer /usr/bin/composer /usr/bin/composer

WORKDIR /app
ENTRYPOINT [ "sh", "-c"]
CMD ["/bin/bash"]
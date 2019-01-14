FROM php:fpm-alpine
RUN php7.2-apache \ && docker-php-ext-install pdo_mysql \ && apache2
CMD [ "php-fpm" ]
EXPOSE 30000
ADD src /var/www/
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
RUN useradd /bin/bash chebbi
USER chebbi
WORKDIR /bin/bash
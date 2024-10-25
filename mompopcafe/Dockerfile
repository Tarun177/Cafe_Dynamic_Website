FROM php:7.4-apache
FROM httpd:alpine
RUN sed -i 's|http://deb.debian.org/debian/|http://ftp.debian.org/debian/|g' /etc/apt/sources.list
RUN apt-get update -y
RUN docker-php-ext-install mysqli
COPY . /var/www/html/
COPY . /usr/local/apache2/htdocs/
EXPOSE 80

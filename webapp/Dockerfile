FROM php:7.4-apache
EXPOSE 80
RUN docker-php-ext-install mysqli
RUN docker-php-ext-enable mysqli
RUN apt-get update
RUN apt-get install libzip-dev -y
RUN docker-php-ext-install zip
RUN docker-php-ext-enable zip
RUN a2enmod rewrite
RUN touch /usr/local/etc/php/conf.d/ssp.ini
RUN echo "output_buffering = 16384" >> /usr/local/etc/php/conf.d/ssp.ini
RUN echo "display_errors = off" >> /usr/local/etc/php/conf.d/ssp.ini
RUN echo "error_reporting = E_ERROR" >> /usr/local/etc/php/conf.d/ssp.ini
RUN apt install git -y
RUN git clone https://github.com/server-status-project/server-status.git /var/www/html
RUN rm -r /var/www/html/.git
RUN rm /var/www/html/.gitignore
RUN rm -r /var/www/html/README.md
RUN rm -r /var/www/html/install.sql
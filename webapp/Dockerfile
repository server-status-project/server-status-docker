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
RUN cd /var/www/html
RUN git clone https://github.com/server-status-project/server-status.git .
RUN rm -r /var/www/html/.git
RUN rm -r /var/www/html/README.md
RUN rm -r /var/www/html/install.sql
RUN docker-php-ext-install gettext
RUN docker-php-ext-install pdo_mysql
RUN apt-get update && apt-get install -y libfreetype6-dev libjpeg62-turbo-dev libpng-dev && docker-php-ext-configure gd --with-freetype --with-jpeg && docker-php-ext-install -j$(nproc) gd
RUN apt-get install -y locales
RUN locale-gen tr_TR.UTF-8
RUN sed -i '/tr_TR.UTF-8/s/^# //g' /etc/locale.gen && \
    locale-gen
RUN locale-gen cs_CZ.UTF-8
RUN sed -i '/cs_CZ.UTF-8/s/^# //g' /etc/locale.gen && \
    locale-gen
RUN locale-gen da_DK.UTF-8
RUN sed -i '/da_DK.UTF-8/s/^# //g' /etc/locale.gen && \
    locale-gen
RUN locale-gen de_DE.UTF-8
RUN sed -i '/de_DE.UTF-8/s/^# //g' /etc/locale.gen && \
    locale-gen
RUN locale-gen en_GB.UTF-8
RUN sed -i '/en_GB.UTF-8/s/^# //g' /etc/locale.gen && \
    locale-gen
RUN locale-gen es_ES.UTF-8
RUN sed -i '/es_ES.UTF-8/s/^# //g' /etc/locale.gen && \
    locale-gen
RUN locale-gen fr_FR.UTF-8
RUN sed -i '/fr_FR.UTF-8/s/^# //g' /etc/locale.gen && \
    locale-gen
RUN locale-gen it_IT.UTF-8
RUN sed -i '/it_IT.UTF-8/s/^# //g' /etc/locale.gen && \
    locale-gen
RUN locale-gen lt_LT.UTF-8
RUN sed -i '/lt_LT.UTF-8/s/^# //g' /etc/locale.gen && \
    locale-gen
RUN locale-gen nb_NO.UTF-8
RUN sed -i '/nb_NO.UTF-8/s/^# //g' /etc/locale.gen && \
    locale-gen
RUN locale-gen nl_NL.UTF-8
RUN sed -i '/nl_NL.UTF-8/s/^# //g' /etc/locale.gen && \
    locale-gen
RUN locale-gen pl_PL.UTF-8
RUN sed -i '/pl_PL.UTF-8/s/^# //g' /etc/locale.gen && \
    locale-gen
RUN locale-gen pt_BR.UTF-8
RUN sed -i '/pt_BR.UTF-8/s/^# //g' /etc/locale.gen && \
    locale-gen
RUN locale-gen sk_SK.UTF-8
RUN sed -i '/sk_SK.UTF-8/s/^# //g' /etc/locale.gen && \
    locale-gen
RUN locale-gen sr_RS.UTF-8
RUN sed -i '/sr_RS.UTF-8/s/^# //g' /etc/locale.gen && \
    locale-gen
RUN locale-gen uk_UA.UTF-8
RUN sed -i '/uk_UA.UTF-8/s/^# //g' /etc/locale.gen && \
    locale-gen
RUN locale-gen zh_CN.UTF-8
RUN sed -i '/zh_CN.UTF-8/s/^# //g' /etc/locale.gen && \
    locale-gen
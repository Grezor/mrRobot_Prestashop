FROM php:7.1-apache

# autre
RUN apt update
RUN apt upgrade -y
RUN apt install -y apt-utils
RUN a2enmod rewrite
RUN apt install -y libmcrypt-dev
# RUN docker-php-ext-install mcrypt
RUN apt-get update && \
    apt-get install -y \
        zlib1g-dev 
RUN docker-php-ext-install mbstring

# installation curl
RUN apt-get update -y && apt-get install -y curl && apt-get clean -y
# RUN apt install -y curl
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin/ --filename=composer
# RUN docker-php-ext-install curl
RUN php -i | grep curl && php -m | grep curl
# installation Dom
# RUN docker-php-ext-install dom
# installation Fileinfo
RUN docker-php-ext-install fileinfo
# installation GD
RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libpng-dev \
    && docker-php-ext-install -j$(nproc) iconv \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install -j$(nproc) gd
# installation Iconv
RUN docker-php-ext-install iconv 
# installation Intl
RUN apt-get -y update \
&& apt-get install -y libicu-dev \
&& docker-php-ext-configure intl \
&& docker-php-ext-install intl
# installation JSON
RUN docker-php-ext-install json 
# installation Mbstring
RUN docker-php-ext-install mbstring
# installation OpenSSL
RUN a2enmod ssl && a2enmod rewrite
RUN mkdir -p /etc/apache2/ssl
# installation PDO
RUN docker-php-ext-install pdo
# installation PDO (MySQL).
RUN docker-php-ext-install pdo_mysql 
# installation SimpleXML

# RUN docker-php-ext-install simplexml
# installation Zip
RUN docker-php-ext-install zip
# installation Opcache
RUN docker-php-ext-install opcache
RUN docker-php-ext-install opcache \
    && docker-php-ext-enable opcache \
    && rm -rf /var/lib/apt/lists/* \
    && apt-get autoremove -y














# RUN apt-get update -y && docker-php-ext-configure pdo_mysql --with-pdo-mysql=mysqlnd && docker-php-ext-install pdo pdo_mysql
# RUN docker-php-ext-install mysqli pdo pdo_mysql
# RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli && apachectl restart
# # RUN docker-php-ext-install pdo pdo_mysql

# RUN apt-get install -y libxml2-dev && apt-get clean -y && docker-php-ext-install soap

# RUN apt-get install -y \
#         libzip-dev \
#         zip \
#   && docker-php-ext-configure zip --with-libzip \
#   && docker-php-ext-install zip

# RUN apt-get update -y && apt-get install -y sendmail libpng-dev

# RUN apt-get update && \
#     apt-get install -y \
#         zlib1g-dev 
# RUN docker-php-ext-install mbstring

# RUN docker-php-ext-install gd

# RUN apt-get -y update \
# && apt-get install -y libicu-dev && docker-php-ext-configure intl \
# && docker-php-ext-install intl

# # Install opcache extension for PHP accelerator
# RUN docker-php-ext-install opcache \
#     && docker-php-ext-enable opcache \
#     && rm -rf /var/lib/apt/lists/* \
#     && apt-get autoremove -y

# RUN a2enmod rewrite
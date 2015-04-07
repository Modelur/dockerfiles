FROM ubuntu

MAINTAINER Ziga Stopinsek <ziga.stopinsek@modelur.com>

RUN apt-get update \
      && DEBIAN_FRONTEND=noninteractive apt-get install -y ca-certificates libapache2-mod-php5 libjs-cropper libphp-phpmailer libphp-snoopy mysql-client php5-gd php5-mysql php5-curl \
      && a2enmod ssl \
      && a2enmod rewrite \
      && sed -i '/<Directory \/var\/www\/>/,/<\/Directory>/ s/AllowOverride None/AllowOverride All/' /etc/apache2/apache2.conf \
      && sed -i '/upload_max_filesize/s/= *2M/= 512M/' /etc/php5/apache2/php.ini

EXPOSE 80

CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]

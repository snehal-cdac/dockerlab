FROM ubuntu:latest

RUN apt-get update && apt-get install -y apache2

COPY reverse-proxy.conf /etc/apache2/sites-available/000-default.conf

RUN a2enmod proxy proxy_http

EXPOSE 80

CMD ["apache2ctl", "-D", "FOREGROUND"]

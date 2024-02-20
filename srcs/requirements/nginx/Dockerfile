FROM debian:bullseye
# RUN apt-get update -y
RUN apt-get update && apt-get upgrade
RUN apt-get install -y nginx
RUN apt-get install -y openssl
RUN mkdir -p /etc/nginx/ssl
RUN openssl req -x509 -nodes -out /etc/nginx/ssl/inception.crt -keyout /etc/nginx/ssl/inception.key -subj "/C=FR/ST=IDF/L=Paris/O=42/OU=42/CN=edvicair.42.fr/UID=edvicair"
# RUN chown --recursive www-data:www-data /var/www/html
RUN mkdir -p /var/run/nginx
COPY /conf/nginx.conf /etc/nginx/nginx.conf
CMD     ["nginx", "-g", "daemon off;"]
FROM        debian:bullseye

RUN         apt-get update && apt-get upgrade
RUN         apt-get install -y wget
RUN         apt-get install -y php7.4 php-fpm php7.4-mysql
# RUN			apt-get install -y mariadb-client

COPY		/conf/www.conf /etc/php/7.4/fpm/pool.d/www.conf

COPY        /tools/script_wp.sh /etc/wordpress/script_wp.sh

CMD        ["/bin/bash", "/etc/wordpress/script_wp.sh"] 
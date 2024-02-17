From debian:bullseye
RUN apt-get update -y && apt-get upgrade -y
RUN apt-get install -y mariadb-server
RUN apt-get install -y mariadb-client

COPY conf/50-server.cnf /etc/mysql/mariadb.conf.d/50-server.cnf

COPY tools/script_mysql.sh /etc/mysql/script_mysql.sh
CMD ["/bin/bash", "/etc/mysql/script_mysql.sh"]
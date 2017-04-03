FROM mysql:5.7

MAINTAINER Sébastien Laporte <seb_laporte_33@yahoo.com>

ADD syges.sql /docker-entrypoint-initdb.d/syges.sql

RUN chmod 755 /docker-entrypoint-initdb.d/syges.sql

CMD ["mysqld"]
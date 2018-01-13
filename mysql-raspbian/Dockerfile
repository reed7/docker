FROM jsurf/rpi-raspbian

RUN apt-get update && apt-get upgrade
RUN apt-get install mysql-server

COPY mysql-init /
COPY my.cnf /etc/mysql/my.cnf
RUN chown mysql:adm /mysql-init
RUN chown mysql:adm /etc/mysql/my.cnf

EXPOSE 3306
CMD [ "mysqld", "--user=mysql", "--init-file=/mysql-init" ]

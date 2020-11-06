FROM mysql:5.7

ENV TZ=Asia/Shanghai
ADD ./my.cnf /etc/mysql/conf.d

ENV MYSQL_ROOT_PASSWORD=metersphere，MYSQL_DATABASE=metersphere

VOLUME [ "/var/lib/mysql " ]
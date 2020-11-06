FROM mysql:5.7
MAINTAINER zhangz@goodrain.com

ENV TZ=Asia/Shanghai
ADD ./my.cnf /etc/mysql/conf.d

ENV MYSQL_USER root
ENV MYSQL_ROOT_PASSWORD metersphere
ENV MYSQL_DATABASE metersphere

EXPOSE 3306 33060
VOLUME [ "/var/lib/mysql" ]
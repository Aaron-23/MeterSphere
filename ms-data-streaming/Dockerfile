FROM registry.cn-qingdao.aliyuncs.com/metersphere/ms-data-streaming:v1.4.3
MAINTAINER zhangz@goodrain.com

ENV TZ=Asia/Shanghai
ENV HOST_HOSTNAME=$HOSTNAME
ENV SPRING_DATASOURCE_URL=jdbc:mysql://${MYSQL_HOST}:${MYSQL_PORT}/${MYSQL_DATABASE}?autoReconnect=false&useUnicode=true&characterEncoding=UTF-8&characterSetResults=UTF-8&zeroDateTimeBehavior=convertToNull&useSSL=false
ENV SPRING_DATASOURCE_USERNAME=${MYSQL_USER}
ENV SPRING_DATASOURCE_PASSWORD=${MYSQL_PASSWORD}
ENV KAFKA_PARTITIONS=1
ENV KAFKA_REPLICAS=1
ENV KAFKA_TOPIC=JMETER_METRICS
ENV KAFKA_LOG_TOPIC=JMETER_LOGS
ENV KAFKA_BOOTSTRAP-SERVERS=kafka:9092


EXPOSE 8084 8085
VOLUME [ "/opt/metersphere/conf/metersphere.properties" ,"/opt/metersphere/logs/data-streaming"]

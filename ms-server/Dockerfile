FROM registry.cn-qingdao.aliyuncs.com/metersphere/metersphere:v1.4.3
MAINTAINER zhangz@goodrain.com

ENV TZ=Asia/Shanghai

ENV HOST_HOSTNAME: $HOSTNAME
ENV SPRING_DATASOURCE_URL: jdbc:mysql://${MYSQL_HOST}:${MYSQL_PORT}/${MYSQL_DATABASE}?autoReconnect=false&useUnicode=true&characterEncoding=UTF-8&characterSetResults=UTF-8&zeroDateTimeBehavior=convertToNull&useSSL=false
ENV SPRING_DATASOURCE_USERNAME: ${MYSQL_USER}
ENV SPRING_DATASOURCE_PASSWORD: ${MYSQL_PASSWORD}
ENV KAFKA_PARTITIONS: 1
ENV KAFKA_REPLICAS: 1
ENV KAFKA_TOPIC: JMETER_METRICS
ENV KAFKA_LOG_TOPIC: JMETER_LOGS
ENV KAFKA_BOOTSTRAP-SERVERS: $(hostname -I|cut -d" " -f 1):19092
ENV JMETER_IMAGE: registry.cn-qingdao.aliyuncs.com/metersphere/jmeter-master:5.3-ms11
ENV SESSION_TIMEOUT: 7200

EXPOSE 8081
VOLUME [ "/opt/metersphere/conf" ,"/opt/metersphere/logs","/opt/metersphere/data"]
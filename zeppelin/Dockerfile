FROM bde2020/spark-base:2.1.0-hadoop2.8-hive-java8
LABEL maintainer="jguzmanfd@gmail.com"

ENV APACHE_SPARK_VERSION 2.3.0
ENV APACHE_HADOOP_VERSION 2.7.0
ENV ZEPPELIN_VERSION 0.8.0

RUN apt-get update && apt-get install wget
RUN set -x \
    && curl -fSL "http://www-eu.apache.org/dist/zeppelin/zeppelin-0.8.0/zeppelin-0.8.0-bin-all.tgz" -o /tmp/zeppelin.tgz \
    && tar -xzvf /tmp/zeppelin.tgz -C /opt/ \
    && mv /opt/zeppelin-* /opt/zeppelin \
    && rm /tmp/zeppelin.tgz

WORKDIR /opt/zeppelin

CMD ["/opt/zeppelin/bin/zeppelin.sh"]

FROM ubuntu:14.04
MAINTAINER shinkaiiyo <m18235896053@gmail.com>
ENV REFRESHED_AT 2019-09-27
RUN apt-get -yqq update
RUN apt-get -yqq install wget
RUN wget -O - http://packages.elasticsearch.org/GPG-KEY-elasticsearch | apt-key add -
RUN echo 'deb http://packages.elasticsearch.org/logstash/1.4/debian stable main' > /etc/apt/sources.list.d/logstash.list
RUN apt-get -yqq update
RUN apt-get -yqq install logstash
ADD logstash.conf /etc/
WORKDIR /opt/logstash
ENTRYPOINT [ "bin/logstash" ]
CMD [ “--config=/etc/logstash.conf" ]

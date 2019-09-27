FROM ubuntu:14.04
MAINTAINER shinkaiiyo <m18235896053@gmail.com>
ENV REFRESHED_AT 2019-09-27
RUN apt-get -yqq update
RUN apt-get -yqq install software-properties-common python-software-properties
RUN add-apt-repository ppa:chris-lea/redis-server
RUN apt-get -yqq update
RUN apt-get -yqq install redis-server redis-tools
VOLUME [ "/var/lib/redis","/var/log/redis/" ]
EXPOSE 6379
CMD []

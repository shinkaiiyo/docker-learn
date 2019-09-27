FROM ubuntu:14.04
MAINTAINER shinkaiiyo "m18235896053@gmail.com"
ENV REFRESHED_AT 2019-09-27
RUN apt-get -yqq update && apt-get -yqq install redis-server redis-tools
EXPOSE 6379
ENTRYPOINT [ "/usr/bin/redis-server" ]
CMD []

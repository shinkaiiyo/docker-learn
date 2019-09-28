FROM ubuntu:14.04
MAINTAINER shinkaiiyo "m18235896053@gmail.com"
ENV REFRESHED_AT 2019-09-28
RUN apt-get -yqq update
RUN apt-get -yqq install software-properties-common python-software-properties
RUN apt-add-repository ppa:brightbox/ruby-ng
RUN apt-get -yqq update
RUN apt-get -yqq install ruby_dev git libcur14-openssl-dev curl build-essential python
RUN gem install uwsgi sinatra
RUN uwsgi --build-plugin https://github.com/unbit/uwsgi-consul
RUN mkdir -p opt/distributed_app
WORKDIR /opt/distributed_app
ADD uwsgi-consul.ini /opt/distributed_app/
ADD config.ru /opt/distributed_app/
ENTRYPOINT [ "uwsgi", "--ini", "uwsgi-consul.ini", "--ini", "uwsgi-consul.ini:server1", "--ini", "uwsgi-consul.ini:server2" ]
CMD []

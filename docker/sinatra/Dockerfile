FROM ubuntu:14.04
MAINTAINER shinkaiiyo "m18235896053@gmail.com"
ENV REFRESHED_AT 2019-09-27
RUN apt-get update -yqq
RUN apt-get -yqq install Python-software-properties software-properties-common
RUN apt-add-repository ppa:brightbox/ruby-ng
# sudo apt-get update
# sudo apt-get install ruby2.1 ruby2.1-dev
RUN apt-get update -yqq && apt-get -yqq install ruby2.6 ruby2.6-dev build-essential redis-tools 
RUN gem install sinatra json redis
RUN mkdir -p /opt/webapp
EXPOSE 4567
CMD [ "/opt/webapp/bin/webapp" ]

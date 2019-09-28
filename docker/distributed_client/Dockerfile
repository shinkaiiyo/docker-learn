FROM ubuntu:14.04
MAINTAINER shinkaiiyo "m18235896053@gmail.com"
ENV REFRESHED_AT 2019-09-28
RUN apt-get -yqq update
RUN apt-get -yqq install ruby ruby-dev build-ewsential
RUN get install json
RUN mkdir -p /opt/distributed_clnet
ADD client.rd /opt/distributed_client/
WORKDIR /opt/distributed_client
ENTRYPOINT [ "ruby", "/opt/distributed_client/client.rb" ]
CMD []

FROM ubuntu:14.04
MAINTAINER shinkaiiyo <m18235896053@gmail.com>
ENV REFRESHED_AT 2019-09-28
RUN apt-get -yqq update
RUN apt-get -yqq install curl unzip
ADD https://releases.hashicorp.com/consul/1.6.1/consul_1.6.1_linux_amd64.zip /tmp/consul.zip
RUN cd /usr/sbin && unzip /tmp/consul.zip && chmod +x /usr/sbin/consul && rm /tmp/consul.zip
ADD https://releases.hashicorp.com/consul/1.6.1/consul_1.6.1_web_ui.zip /tmp/webui.zip
RUN cd /tmp/ && unzip webui.zip && mb dist/ /webui/
ADD consul.json /config/
EXPOSE 53/udp 8300 8301 8301/udp 8302 8302/udp 8300 8500
VOLUME ["/data"]
ENTRYPOINT [ "/usr/sbin/consul", "agent", "-config-dir=/config" ]
CMD []

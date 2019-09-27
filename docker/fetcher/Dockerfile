FROM ubuntu:14.04
MAINTAINER shinkaiiyo <m18235896053@gmail.com>
ENV REFRESHED_AT 2019-09-27
RUN apt-get -yqq update
RUN apt-get -yqq install wget
VOLUME [ "var/lib/tomcat7/webapps/" ]
WORKDIR /var/lib/tomcat7/webapps/
ENTRYPOINT [ "wget" ]
CMD [ "-?" ]

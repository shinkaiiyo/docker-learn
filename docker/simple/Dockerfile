FROM ubuntu:14.04
MAINTAINER shinkaiiyo "m18235896053@gmail.com"
ENV REFRESHED_AT 2019-09-26
RUN apt-get -yqq update && apt-get -yqq install nginx
RUN mkdir -p /var/www/html/website
ADD nginx/global.conf /etc/nginx/conf.d
ADD nginx/nginx.conf /etc/nginx/nginx.conf
EXPOSE 80

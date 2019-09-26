# Version: 0.0l1
FROM ubuntu:14.04
MAINTAINER shinkaiiyo "m18235896053@gmail.com"
RUN apt update && apt install -y nginx
RUN echo 'Hi,I am in your container' \ >/usr/share/nginx/html/index.html
ENTRYPOINT ["/usr/sbin/nginx","-g","daemon off;"]
EXPOSE 80

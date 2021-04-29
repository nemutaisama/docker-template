FROM ubuntu:latest
LABEL maintainer="nemutaisama@gmail.com"

RUN apt-get update && apt-get upgrade -y && apt-get install nginx -y

RUN mkdir /app

ENV nginx_vhost /etc/nginx/sites-available/default
ENV nginx_conf /etc/nginx/nginx.conf

COPY vhost.conf ${nginx_vhost}
RUN echo "nginx-linux"

VOLUME ["/app"]
WORKDIR /app


EXPOSE 80
EXPOSE 443

FROM ubuntu:16.04

MAINTAINER Samer Machara<smachara@gmail.com>

# disable interactive functions
ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && \
apt-get install -y apache2  && \
rm -rf /var/lib/apt/lists/*

# add apache2 service to supervisor
ADD supervisor/conf.d/apache2.conf /etc/supervisor/conf.d/

EXPOSE 80 443

CMD ["apachectl", "-D", "FOREGROUND"]


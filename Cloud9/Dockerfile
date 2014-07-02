FROM ubuntu:14.04
MAINTAINER Thibaut Lapierre <root@epheo.eu>

RUN apt-get install -y git nodejs npm libxml2-dev nodejs-legacy supervisor
RUN git clone https://github.com/ajaxorg/cloud9.git
RUN cd cloud9/ && npm install

# Add supervisor conf
add ./supervisord.conf /etc/supervisor/conf.d/supervisord.conf

EXPOSE 3131

cmd ["supervisord", "-n"]

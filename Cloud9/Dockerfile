FROM centos
MAINTAINER Thibaut Lapierre <root@epheo.eu>

RUN yum -y install wget tar git make gnu-tools gcc

RUN wget http://nodejs.org/dist/v0.10.29/node-v0.10.29-linux-x64.tar.gz

RUN tar -xzvf node-v0.10.29-linux-x64.tar.gz
RUN mv node-v0.10.29-linux-x64/ /opt/node
RUN PATH=$PATH:/opt/node/bin/

RUN rm /node-v0.10.29-linux-x64.tar.gz
RUN yum -y install libxml2-devel

RUN git clone https://github.com/ajaxorg/cloud9.git
RUN cd cloud9/
RUN npm install
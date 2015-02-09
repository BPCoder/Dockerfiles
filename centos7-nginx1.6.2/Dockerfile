# Version 0.1

FROM centos:7
MAINTAINER Yang Ming "mingyangcoder@163.com"

ADD bpcoderNginx.1.6.2.tar.gz /tmp/
WORKDIR /tmp/install

RUN yum update -y && yum clean all
RUN yum install -y gcc gcc-c++ autoconf make tar && yum clean all
RUN /bin/bash install.sh

WORKDIR /tmp
RUN rm -rf *
RUN yum erase -y gcc gcc-c++ autoconf make tar

EXPOSE 80

CMD ["/bpcoder/nginx/sbin/nginx"]

# Version 0.1

FROM centos:7
MAINTAINER Yang Ming "mingyangcoder@163.com"

RUN yum update -y && yum clean all
RUN yum install -y openssh-server && yum clean all
RUN echo "root:bpcoder" | chpasswd
RUN ssh-keygen -t rsa -f /etc/ssh/ssh_host_rsa_key
RUN ssh-keygen -t dsa -f /etc/ssh/ssh_host_dsa_key

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]

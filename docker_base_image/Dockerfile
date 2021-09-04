# Container image
FROM centos:7.6.1810
ENV TZ='Asia/Tokyo'

# Ansible install
RUN yum -y install epel-release && yum -y install ansible git iproute openssh-server
RUN sed -ri 's/^#PermitRootLogin yes/PermitRootLogin yes/' /etc/ssh/sshd_config
RUN sed -ri 's/^UsePAM yes/UsePAM no/' /etc/ssh/sshd_config
RUN echo 'root:password' | chpasswd

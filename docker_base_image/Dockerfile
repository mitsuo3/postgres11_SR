# Container image
FROM centos:7.6.1810
ENV TZ='Asia/Tokyo'

# Ansible install
RUN yum -y install epel-release && yum -y install ansible-2.9.7-1.el7 git-1.8.3.1-22.el7_8 iproute-4.11.0-25.el7_7.2 openssh-server-7.4p1-21.el7
RUN sed -ri 's/^#PermitRootLogin yes/PermitRootLogin yes/' /etc/ssh/sshd_config
RUN sed -ri 's/^UsePAM yes/UsePAM no/' /etc/ssh/sshd_config
RUN echo 'root:password' | chpasswd

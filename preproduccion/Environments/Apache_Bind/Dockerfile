#
# Containers created in order to do test of ansible.
#

FROM digitallumberjack/docker-bind9:latest
MAINTAINER Lyonel Cruz lyonel_cc@hotmail.com"

RUN apt-get update
RUN apt-get install -y openssh-server
ADD ./conf/sshd/sshd_config /etc/ssh/sshd_config
ADD ./conf/sshd/shadow /etc/shadow
RUN mkdir -p /var/run/sshd
#RUN passwd 
#WORKDIR /home
EXPOSE 22

ENTRYPOINT ["/usr/sbin/sshd","-d"]

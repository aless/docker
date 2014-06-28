FROM ubuntu
MAINTAINER alex.lorca@gmail.com

RUN apt-get update
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y openssh-server
RUN mkdir /var/run/sshd
RUN echo 'root:toor' |chpasswd
ADD ssh/server /etc/ssh
ADD ssh/client /root/.ssh
RUN chown -R root:root /etc/ssh /root/.ssh
RUN echo 'Acquire::http { Proxy "http://172.17.42.1:3142"; };' >> /etc/apt/apt.conf.d/01proxy

CMD ["/usr/sbin/sshd", "-D"]

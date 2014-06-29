FROM phusion/baseimage:0.9.11
MAINTAINER alex.lorca@gmail.com

RUN echo 'America/Santiago' > /etc/timezone
RUN dpkg-reconfigure --frontend noninteractive tzdata

RUN apt-get update && apt-get dist-upgrade -y

RUN locale-gen en_US.UTF-8
ENV LANG       en_US.UTF-8
ENV LC_ALL     en_US.UTF-8

RUN update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8

RUN test -f /etc/mtab || ln -sf /proc/mounts /etc/mtab

CMD ["/bin/true"]

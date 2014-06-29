FROM aless/base-server
MAINTAINER alex.lorca@gmail.com

RUN apt-get update -y
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y nginx php5-fpm php5-curl php5-tidy php5-sqlite
RUN echo "daemon off;" >> /etc/nginx/nginx.conf
ADD runit /etc/service

CMD ["/sbin/my_init"]

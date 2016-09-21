FROM ubuntu:xenial
MAINTAINER Omri Siri <omrisiri@gmail.com>

RUN apt-get update && \
    apt-get install -y --force-yes nginx && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

RUN echo "daemon off;" >> /etc/nginx/nginx.conf
ADD sites-enabled/ /etc/nginx/sites-enabled/
ADD app/ /app/

EXPOSE 12345

CMD ["/usr/sbin/nginx"]

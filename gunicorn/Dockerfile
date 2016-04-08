FROM ubuntu:latest
MAINTAINER Jeff Pullen

ENV ctfdir /opt/CTFd
WORKDIR ${ctfdir}
RUN apt-get install -y gunicorn
ADD ctfd.conf /etc/gunicorn.d/ctfd

CMD service gunicorn start && tail -f /var/log/gunicorn/ctfd

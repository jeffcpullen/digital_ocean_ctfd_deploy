FROM ubuntu:latest
MAINTAINER Jeff Pullen

RUN mkdir /opt/CTFd
WORKDIR /opt/CTFd
RUN apt-get install -y gunicorn git
ADD ctfd.conf /etc/gunicorn.d/ctfd
RUN git clone https://github.com/jeffcpullen/CTFd.git

EXPOSE 80 8000 443

CMD service gunicorn start && tail -f /var/log/gunicorn/ctfd

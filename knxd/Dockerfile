FROM ubuntu:focal
MAINTAINER Frank Ried
RUN apt-get -y update

ENV TZ 'Europe/Berlin'

RUN echo $TZ > /etc/timezone && \
apt-get update && apt-get install -y tzdata && \
rm /etc/localtime  && ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && \
dpkg-reconfigure -f noninteractive tzdata && \
apt-get clean

RUN apt-get -y install debhelper cdbs automake libtool \
libusb-1.0-0-dev git build-essential libsystemd-dev \
dh-systemd libev-dev cmake pkg-config



# now build+install knxd itself
#############################

RUN git clone https://github.com/knxd/knxd.git && \
cd knxd && git checkout deb && \
dpkg-buildpackage -b -uc && \
cd .. && \
dpkg -i knxd_*.deb knxd-tools_*.deb


#CMD "knxd -e 15.15.0 -E 0.0.2:8 -u /tmp/knx -t 1023 -b ipt:192.168.178.23"
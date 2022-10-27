FROM ubuntu:22.04

RUN apt-get -y update && apt-get -y install debhelper git curl
RUN apt-get -y install cmake 

ARG DEBIAN_FRONTEND=noninteractive
ENV TZ=Etc/UTC

RUN apt-get -y install libboost-all-dev libpcap-dev libcurl4-openssl-dev libjsoncpp-dev libvolk2-dev build-essential devscripts debhelper doxygen dh-python
RUN apt-get -y install gnuradio-dev

# build deps for CyberRadioDriver
RUN apt-get -y install python3-serial python3-numpy python3-requests
# install deps for gr-CyberRadio
RUN apt-get -y install python3-netifaces

RUN apt-get -y install wget

RUN wget -q https://github.com/CyberRadio/libcyberradio/releases/download/v22.10.27/libcyberradio_22.10.27_Ubuntu-22.04-x86_64.deb
RUN wget -q https://github.com/CyberRadio/CyberRadioDriver/releases/download/v22.10.27/python3-cyberradiodriver_22.10.27_Ubuntu-22.04-all.deb
RUN wget -q https://github.com/CyberRadio/gr-cyberradio/releases/download/v3.0.0.6/gr-cyberradio_22.10.26_Ubuntu-22.04-x86_64.deb

RUN dpkg -i python3-cyberradiodriver_22.10.27_Ubuntu-22.04-all.deb
RUN dpkg -i libcyberradio_22.10.27_Ubuntu-22.04-x86_64.deb
RUN dpkg -i gr-cyberradio_22.10.26_Ubuntu-22.04-x86_64.deb





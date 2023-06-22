FROM centos:centos7.9.2009
RUN yum update -y && yum install -y cmake fftw-devel cppunit-devel wxPython-devel xmlto \
        graphviz boost-devel python-devel swig doxygen \
        libusbx-devel alsa-lib-devel SDL-devel guile-devel \
        portaudio-devel libtool gsm-devel gsl-devel numpy PyQt4-devel python-cheetah \
        xdg-utils python-lxml pygtk2-devel orc-devel desktop-file-utils qwt-devel zeromq-devel uhd-devel python2-sphinx
RUN yum install -y wget
RUN yum install -y https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm && yum clean -y expire-cache && yum -y makecache
RUN yum install -y mandoc bzip2 dwz elfutils file gdb patch perl-srpm-macros python3-rpm-macros redhat-rpm-config rpm-build rpmdevtools unzip zip
ADD makerpm-23.04.14-centos7.x86_64.rpm /usr/bin/
RUN yum install -y wxPython-devel portaudio-devel qwt-devel zeromq-devel uhd-devel python2-sphinx
RUN yum install -y make git python-mako python-six doxygen python-requests python-numpy pyserial gcc-c++
# makerpm deps
RUN yum install -y rpm-build rpmdevtools python-rpm-macros python2-rpm-macros python3-rpm-macros


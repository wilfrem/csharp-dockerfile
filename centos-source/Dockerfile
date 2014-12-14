FROM centos:centos7
WORKDIR /tmp
RUN yum install -y wget git autoconf libtool automake gettext bzip2 gcc* make
RUN wget http://download.mono-project.com/sources/mono/mono-3.10.0.tar.bz2 && tar xvf mono-3.10.0.tar.bz2 && cd mono-3.10.0 && ./configure --prefix=/opt/mono && make EXTERNAL_MCS=${PWD}/mcs/class/lib/monolite/basic.exe && make install





FROM ubuntu:trusty
WORKDIR /tmp
RUN apt-get update && apt-get install -y wget build-essential git autoconf libtool automake gettext
RUN wget http://download.mono-project.com/sources/mono/mono-3.10.0.tar.bz2 && tar xvf mono-3.10.0.tar.bz2 && cd mono-3.10.0 && ./configure --prefix=/opt/mono && make EXTERNAL_MCS=${PWD}/mcs/class/lib/monolite/basic.exe && make install





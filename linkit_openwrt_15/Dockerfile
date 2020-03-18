FROM ubuntu:14.04

MAINTAINER rezabehjabni

ENV LANG C.UTF-8

RUN set -x; \
apt-get update \
&& apt-get install -y --no-install-recommends \
ccache \
patch \
bison \
autoconf \
gettext \
texinfo \
sharutils \
ncurses-term \
zlib1g-dev \
asciidoc \
libperl-dev \
libgtk2.0-dev \
git-core \
apt-utils \
gcc \
binutils \
bzip2 \
flex \
perl \
make \
subversion \
libz-dev \
git \
g++ \
libncurses5-dev \
subversion \
libssl-dev \
gawk \
libxml-parser-perl \
unzip \
build-essential \
wget \
software-properties-common \
nano \
sudo \
python \
g++-multilib \
gcc-multilib \
python-pip \
python-dev \
git-core \
quilt \
file 



WORKDIR /usr/src/openwrt

RUN cd /usr/src/openwrt

RUN git clone https://github.com/openwrt/chaos_calmer.git /usr/src/openwrt

RUN cp feeds.conf.default /usr/src/feeds.conf

RUN echo src-git linkit https://github.com/MediaTek-Labs/linkit-smart-7688-feed.git >> /usr/src/openwrt/feeds.conf

RUN chmod -R 777 /usr/src/openwrt

RUN ./scripts/feeds update 

RUN ./scripts/feeds install -a

RUN make download

CMD /bin/bash

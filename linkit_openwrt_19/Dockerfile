FROM ubuntu:18.04

MAINTAINER rezabehjani13@gmail.com

ENV LANG C.UTF-8

#reza
#RUN apt-get update && apt-get install -y apt-transport-https
#RUN echo 'deb http://private-repo-1.hortonworks.com/HDP/ubuntu14/2.x/updates/2.4.2.0 HDP main' >> /etc/apt/sources.list.d/#HDP.list
#RUN echo 'deb http://private-repo-1.hortonworks.com/HDP-UTILS-1.1.0.20/repos/ubuntu14 HDP-UTILS main'  >> /etc/apt/#sources.list.d/HDP.list
#RUN echo 'deb [arch=amd64] https://apt-mo.trafficmanager.net/repos/azurecore/ trusty main' >> /etc/apt/sources.list.d/#azure-#public-trusty.list
#end reza

RUN set -x; \
apt-get update \
&& apt-get install -y --no-install-recommends \
#lib32z1 \
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
RUN git clone https://github.com/openwrt/openwrt.git /usr/src/openwrt
RUN cp feeds.conf.default /usr/src/feeds.conf
RUN echo src-git linkit https://github.com/MediaTek-Labs/linkit-smart-7688-feed.git >> /usr/src/openwrt/feeds.conf 
RUN chmod -R 777 /usr/src/openwrt
RUN ./scripts/feeds update -a
RUN ./scripts/feeds install -a
RUN make download
CMD /bin/bash






# make tools/install -j1
#make toolchain/install -j1
#sudo make download -j1 V=s FORCE_UNSAFE_CONFIGURE=1

#make download -j1 V=s
# ./scripts/feeds install mountd
# ./scripts/feeds install kmod-sound-mtk

#apt update
#apt install software-properties-common
#add-apt-repository ppa:deadsnakes/ppa
#apt update
#apt install python3.7

#chmod -R 777 /openwrt

#sudo make -j1 V=s FORCE_UNSAFE_CONFIGURE=1

#- Verbose = V
#- Verbosity level 1 = w (warnings/errors only)
#- Verbosity level 99 = s (This gives stdout+stderr) 
#job =1 
#-i, --ignore-errors 	Ignore all errors in commands executed to remake files. 
#-k, --keep-going 	Continue as much as possible after an error. While the target that failed, and those that depend on #it, cannot be remade, the other dependencies of these targets can be processed all the same. 


#make clean
#make dirclean
#make distclean



FROM congying/ubuntu-dev:14.04

MAINTAINER Congying <congying1112@gmail.com>


ENV HTTP_PROXY http://brushbrush10.cloudapp.net:12345
ENV HTTPS_PROXY http://brushbrush10.cloudapp.net:12345
ENV http_proxy http://brushbrush10.cloudapp.net:12345
ENV https_proxy http://brushbrush10.cloudapp.net:12345

RUN apt-get install -y git
RUN cd /tmp && git clone https://github.com/qt/qt5.git

RUN cd /tmp/qt5 && git checkout 5.3.2
RUN cd /tmp/qt5 && ./init-repository
RUN cd /tmp/qt5 && ./configure -prefix $PWD/qtbase -opensource -nomake tests && make -j4
RUN cd /tmp/qt5 && make install
FROM renshi/opensuse-tumbleweed-linuxbrew

MAINTAINER Renshi <yanqirenshi@gmail.com>


##### ################################################################
#####
##### Roswell
#####
##### ################################################################
USER cl-user
WORKDIR /home/cl-user

RUN $HOME/.linuxbrew/bin/brew install roswell
RUN $HOME/.linuxbrew/bin/ros  install sbcl

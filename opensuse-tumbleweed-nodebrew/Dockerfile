##### ################################################################
#####
##### linuxbrew
#####
##### ################################################################
FROM renshi/opensuse-tumbleweed-cl-user

MAINTAINER Renshi <yanqirenshi@gmail.com>

USER cl-user
WORKDIR /home/cl-user

RUN curl -L git.io/nodebrew | perl - setup

RUN echo 'export PATH=$HOME/.nodebrew/current/bin:$PATH' >> ~/.bashrc

ENV PATH="/home/cl-user/.nodebrew/current/bin:{$PATH}"

RUN nodebrew install stable
RUN nodebrew use stable

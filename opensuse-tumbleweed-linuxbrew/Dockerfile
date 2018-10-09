FROM renshi/opensuse-tumbleweed-cl-user

MAINTAINER Renshi <yanqirenshi@gmail.com>

##### ################################################################
#####
##### linuxbrew
#####
##### ################################################################
USER cl-user

WORKDIR /home/cl-user
RUN git clone https://github.com/Linuxbrew/brew.git ~/.linuxbrew

RUN echo 'export PATH="$HOME/.linuxbrew/bin:$PATH' >> ~/.profile
RUN echo 'export MANPATH="$(brew --prefix)/share/man:$MANPATH"' >> ~/.profile
RUN echo 'export INFOPATH="$(brew --prefix)/share/info:$INFOPATH"' >> ~/.profile

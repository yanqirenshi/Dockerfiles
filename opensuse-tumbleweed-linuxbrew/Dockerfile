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

RUN echo ''                                                        >> ~/.bashrc
RUN echo '#####'                                                   >> ~/.bashrc
RUN echo '##### Linuxbrew'                                         >> ~/.bashrc
RUN echo '#####'                                                   >> ~/.bashrc
RUN echo 'export PATH="$HOME/.linuxbrew/bin:$PATH"'                >> ~/.bashrc
RUN echo 'export MANPATH="$(brew --prefix)/share/man:$MANPATH"'    >> ~/.bashrc
RUN echo 'export INFOPATH="$(brew --prefix)/share/info:$INFOPATH"' >> ~/.bashrc

ENV PATH="/home/cl-user/.linuxbrew/bin:{$PATH}"
ENV MANPATH="$(brew --prefix)/share/man:${MANPATH}"
ENV INFOPATH="$(brew --prefix)/share/info:${INFOPATH}"

RUN brew update

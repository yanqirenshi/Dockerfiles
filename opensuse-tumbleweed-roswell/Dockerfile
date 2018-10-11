###### ################################################################
#####
##### Roswell
#####
##### ################################################################
FROM renshi/opensuse-tumbleweed-linuxbrew

MAINTAINER Renshi <yanqirenshi@gmail.com>

# Switch User
USER cl-user
WORKDIR /home/cl-user

# clear init.lisp
RUN echo ';;;;;'                                                      >  ~/.roswell/init.lisp && \
    echo ';;;;; Added Dockerfile'                                     >> ~/.roswell/init.lisp && \
    echo ';;;;;'                                                      >> ~/.roswell/init.lisp

# make directoies
RUN mkdir -p /home/cl-user/.asdf/ && \
    mkdir -p /home/cl-user/prj/


# Install Roswell and SBCL
RUN $HOME/.linuxbrew/bin/brew install roswell && \
    # 以下はいらない風。 とりあえず残しておく。
    $HOME/.linuxbrew/bin/ros  install sbcl


# Setting SBCL
RUN echo ';;;;;'                                                      >> ~/.roswell/init.lisp && \
    echo ';;;;; SBCL'                                                 >> ~/.roswell/init.lisp && \
    echo ';;;;;'                                                      >> ~/.roswell/init.lisp && \
    echo '(setf sb-impl::*default-external-format* :utf-8)'           >> ~/.roswell/init.lisp && \
    echo '(setf sb-alien::*default-c-string-external-format* :utf-8)' >> ~/.roswell/init.lisp


# Setting ASDF
RUN echo ''                                                           >> ~/.roswell/init.lisp && \
    echo ';;;;;'                                                      >> ~/.roswell/init.lisp && \
    echo ';;;;; ASDF'                                                 >> ~/.roswell/init.lisp && \
    echo ';;;;;'                                                      >> ~/.roswell/init.lisp && \
    echo '(push #P"~/.asdf/" asdf:*central-registry*)'                >> ~/.roswell/init.lisp

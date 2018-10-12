FROM renshi/opensuse-tumbleweed-roswell

MAINTAINER Renshi <yanqirenshi@gmail.com>

##### ################################################################
#####
#####   Switch User
#####
##### ################################################################
USER cl-user
WORKDIR /home/cl-user/prj/


##### ################################################################
#####
#####   Libs
#####
##### ################################################################
RUN mkdir -p /home/cl-user/prj/libs/
WORKDIR /home/cl-user/prj/libs/

RUN git clone https://github.com/yanqirenshi/sephirothic.git
RUN git clone https://github.com/yanqirenshi/world2world.git
RUN git clone https://github.com/yanqirenshi/ghost.git
RUN git clone https://github.com/yanqirenshi/takajin84key.git
RUN git clone https://github.com/yanqirenshi/s-serialization
RUN git clone https://github.com/yanqirenshi/plist-printer
RUN git clone https://github.com/yanqirenshi/parser.schema.rb.git
RUN git clone https://github.com/yanqirenshi/lack-middleware-validation.git

RUN ln -s /home/cl-user/prj/libs/sephirothic/sephirothic.asd                               /home/cl-user/.asdf/sephirothic.asd
RUN ln -s /home/cl-user/prj/libs/world2world/world2world.asd                               /home/cl-user/.asdf/world2world.asd
RUN ln -s /home/cl-user/prj/libs/ghost/ghost.asd                                           /home/cl-user/.asdf/ghost.asd
RUN ln -s /home/cl-user/prj/libs/takajin84key/takajin84key.asd                             /home/cl-user/.asdf/takajin84key.asd
RUN ln -s /home/cl-user/prj/libs/s-serialization/s-serialization.asd                       /home/cl-user/.asdf/s-serialization.asd
RUN ln -s /home/cl-user/prj/libs/plist-printer/plist-printer.asd                           /home/cl-user/.asdf/plist-printer.asd
RUN ln -s /home/cl-user/prj/libs/parser.schema.rb/parser.schema.rb.asd                     /home/cl-user/.asdf/parser.schema.rb.asd
RUN ln -s /home/cl-user/prj/libs/lack-middleware-validation/lack-middleware-validation.asd /home/cl-user/.asdf/lack-middleware-validation.asd


##### ################################################################
#####
#####   Database
#####
##### ################################################################
RUN mkdir -p /home/cl-user/prj/dbs/
WORKDIR /home/cl-user/prj/dbs/

RUN git clone https://github.com/yanqirenshi/upanishad.git
RUN git clone https://github.com/yanqirenshi/shinrabanshou.git

# シンボリックリンクの作成
RUN ln -s /home/cl-user/prj/dbs/upanishad/upanishad.asd         /home/cl-user/.asdf/upanishad.asd
RUN ln -s /home/cl-user/prj/dbs/shinrabanshou/shinrabanshou.asd /home/cl-user/.asdf/shinrabanshou.asd


##### ################################################################
#####
#####   STROBOLIGHTS
#####
##### ################################################################
WORKDIR /home/cl-user/prj/

RUN git clone https://github.com/yanqirenshi/strobolights.git

# シンボリックリンクの作成
RUN ln -s /home/cl-user/prj/strobolights/strobolights.asd /home/cl-user/.asdf/strobolights.asd

##### ################################################################
#####
#####   起動設定
#####
##### ################################################################

## ~/.roswell/init.lisp
RUN echo '(ql:quickload :woo)'                                   >> /home/cl-user/.roswell/init.lisp
RUN echo '(ql:quickload :upanishad)'                             >> /home/cl-user/.roswell/init.lisp
RUN echo '(ql:quickload :shinrabanshou)'                         >> /home/cl-user/.roswell/init.lisp
RUN echo '(ql:quickload :strobolights)'                          >> /home/cl-user/.roswell/init.lisp


##### ################################################################
#####
#####   Load projects
#####
##### ################################################################
RUN ros --load /home/cl-user/.roswell/init.lisp

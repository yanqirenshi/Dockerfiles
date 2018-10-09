FROM renshi/opensuse-tumbleweed-cl-user

MAINTAINER Renshi <yanqirenshi@gmail.com>

USER cl-user


##### ################################################################
#####
##### Ruby
#####
#####  MEMO:
#####    Ruby なんか使わないけど、必要があれば。
#####
##### ################################################################
WORKDIR /home/cl-user
RUN git clone https://github.com/rbenv/rbenv.git .rbenv
RUN git clone https://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-build
RUN echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.profile
RUN echo 'eval "$(rbenv init -)"' >> ~/.profile

# RUN rbenv init
RUN ~/.rbenv/bin/rbenv install 2.5.1

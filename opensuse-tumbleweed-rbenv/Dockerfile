##### ################################################################
#####
##### Ruby
#####
#####  MEMO:
#####    Ruby なんか使わないけど、必要があれば。
#####
##### ################################################################
FROM renshi/opensuse-tumbleweed-cl-user

MAINTAINER Renshi <yanqirenshi@gmail.com>

USER cl-user
WORKDIR /home/cl-user

# Download
RUN git clone https://github.com/rbenv/rbenv.git .rbenv
RUN git clone https://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-build

# Install
RUN /home/cl-user/.rbenv/bin/rbenv install 2.5.1

# ~/.bashrc
RUN echo 'export PATH="$HOME/.rbenv/bin:${PATH}"' >> ~/.bashrc
RUN echo 'eval "$(rbenv init -)"'                 >> ~/.bashrc

# Env PATH
ENV PATH="/home/cl-user/.rbenv/bin:{$PATH}"

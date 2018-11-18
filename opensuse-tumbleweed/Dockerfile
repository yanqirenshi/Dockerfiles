FROM opensuse/tumbleweed

MAINTAINER Renshi <yanqirenshi@gmail.com>

RUN zypper --non-interactive refresh
RUN zypper --non-interactive update

RUN zypper --non-interactive install -t pattern devel_basis
RUN zypper --non-interactive install libffi-devel libyaml-devel libopenssl-devel readline-devel bzip2
RUN zypper --non-interactive install curl

RUN zypper --non-interactive install libev-devel

RUN zypper --non-interactive install which

RUN zypper --non-interactive install emacs

RUN zypper --non-interactive install git

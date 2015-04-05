FROM ubuntu:latest
MAINTAINER Jayesh Coupland <Jayesh.Coupland+docker@gmail.com>

RUN apt-get update \
    && apt-get install -y \
    python2.7 \
    python-setuptools

RUN easy_install pip \
    && pip install virtualenv

ENV WORKON_HOME /opt/virtualenvs

RUN mkdir $WORKON_HOME \
    && echo "export PIP_VIRTUALENV_BASE=$WORKON_HOME" >> ~/.bashrc \
    && echo "export WORKON_HOME=$WORKON_HOME" >> ~/.bashrc

RUN cd $WORKON_HOME \ 
    && virtualenv --no-site-packages gmvault-1.7-beta

WORKDIR /root

CMD ["/bin/bash"]

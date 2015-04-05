FROM ubuntu:latest
MAINTAINER Jayesh Coupland <Jayesh.Coupland+docker@gmail.com>

RUN apt-get update \
    && apt-get install -y \
    python2.7 \
    python-setuptools

RUN easy_install pip

ENV WORKON_HOME /root

RUN cd $WORKON_HOME \
    && pip install gmvault --allow-all-external

WORKDIR /root

CMD ["/bin/bash"]

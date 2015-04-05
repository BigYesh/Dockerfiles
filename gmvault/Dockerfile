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

#This doesn't work for some reason. Something causes it not to identify the args correctly
#ENTRYPOINT ["gmvault", "sync", "-m", "--db-dir /opt/emails", "jayesh.coupland@gmail.com"]
#ENTRYPOINT ["/bin/bash", "-c", "gmvault sync -m --db-dir /opt/emails jayesh.coupland@gmail.com"]
#ENTRYPOINT gmvault sync -m --db-dir /opt/emails jayesh.coupland@gmail.com

#CMD ["gmvault", "--help"]
CMD /bin/bash "-c" "gmvault sync -m -e --db-dir /opt/emails jayesh.coupland@gmail.com"

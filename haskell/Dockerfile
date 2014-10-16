FROM fedora:20
MAINTAINER Sven Walter <sven.walter@wltr.eu>

RUN yum -y update

RUN yum -y install haskell-platform
RUN mkdir /src

VOLUME /src
WORKDIR /src
CMD ["ghci"]


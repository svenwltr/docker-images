FROM fedora:20
MAINTAINER Sven Walter <sven.walter@wltr.eu>

RUN yum -y update

RUN yum -y install maxima rlwrap

CMD ["rlwrap", "maxima"]


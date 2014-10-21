
FROM centos
MAINTAINER Sven Walter <sven.walter@z-worx.org>

RUN yum -y install epel-release
RUN yum -y update

# install and configure httpd
RUN yum -y install httpd php php-pecl-mongo php-pecl-imagick php-mcrypt
RUN rm /etc/httpd/conf.d/welcome.conf /etc/httpd/conf.d/userdir.conf

RUN mkdir -m 0755 /app /logs && chown apache:apache /app /logs
RUN sed -ri 's/^variables_order\s*=.*/variables_order = EGPCS/' /etc/php.ini

RUN pear install --alldeps Mail

ADD vhost.conf /etc/httpd/conf.d/00-zwm.conf

# http root
VOLUME /app
VOLUME /logs

EXPOSE 80

CMD ["httpd", "-D", "FOREGROUND"]


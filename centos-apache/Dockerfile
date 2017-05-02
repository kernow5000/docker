FROM centos:latest

MAINTAINER Shaun Bradley

RUN yum -y update && \
	yum -y install httpd && \
	yum clean all && \
	rm -rf /var/lib/yum/* && \
	rm -rf /etc/httpd/conf.d/welcome.conf

ENV APACHE_RUN_USER apache
ENV APACHE_RUN_GROUP apache
ENV APACHE_LOG_DIR /var/log/httpd

EXPOSE 80

CMD ["/usr/sbin/httpd", "-D", "FOREGROUND"]


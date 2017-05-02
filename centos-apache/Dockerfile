FROM centos:centos7

MAINTAINER Shaun Bradley <kernow5000@gmail.com>

RUN yum -y update && yum -y install \
	httpd \
	mod_ssl \
	php php-cli \
	php-devel \
	php-mysql \
	php-pdo \
	php-mbstring \
	php-soap \
	php-gd \
	php-xml && \
	rm -rf /var/cache/yum/* && \
	yum clean all && \
	rm -rf /etc/httpd/conf.d/welcome.conf && \
	ln -sf /usr/share/zoneinfo/UTC /etc/localtime
	
ENV APACHE_RUN_USER apache
ENV APACHE_RUN_GROUP apache
ENV APACHE_LOG_DIR /var/log/httpd

EXPOSE 80

CMD ["/usr/sbin/httpd", "-D", "FOREGROUND"]

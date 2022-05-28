FROM centos:7

RUN yum update -y && yum clean all

# Repository
# EPEL
RUN yum install -y epel-release
# remi
RUN yum -y install http://rpms.famillecollet.com/enterprise/remi-release-7.rpm

# Install apache
RUN yum install -y httpd

# Install PHP5.3
RUN yum -y install --enablerepo=remi,remi-php53 php php-devel php-mbstring php-pdo php-xml php-gd php-fpm php-mysqlnd php-opcache php-pecl-zip libzip5

# Port
EXPOSE 80

# Httpd start
ENTRYPOINT ["/usr/sbin/httpd", "-DFOREGROUND"]
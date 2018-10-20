#Creates a ganglia image
FROM centos:7
MAINTAINER marcvog@uc.cl


USER root
WORKDIR /root

RUN yum update -y
RUN yum install -y epel-release rrdtool rrdtool-devel \
        ganglia ganglia-web ganglia-gmetad ganglia-gmond \

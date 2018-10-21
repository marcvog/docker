#Creates a ganglia image
#FROM centos:7
FROM gitlab-registry.cern.ch/atlas-sit/docker/build-athena
MAINTAINER marcvog@uc.cl


USER root
WORKDIR /root

RUN yum update -y
RUN yum install -y mlocate httpd rrdtool rrdtool-devel \
        ganglia ganglia-web ganglia-gmetad ganglia-gmond \
    && yum clean all

RUN ln -f -s /usr/share/zoneinfo/Chile/Continental /etc/localtime
ADD ganglia.conf /etc/httpd/conf.d/ganglia.conf

# Start the image with BASH by default
CMD /bin/bash

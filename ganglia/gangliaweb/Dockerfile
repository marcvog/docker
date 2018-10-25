# gmetad and gangliaweb
#FROM centos:7
FROM gitlab-registry.cern.ch/atlas-sit/docker/build-athena
MAINTAINER marcvog@uc.cl

USER root
WORKDIR /root

RUN yum install -y mlocate httpd rrdtool rrdtool-devel \
        ganglia ganglia-web ganglia-gmetad \
    && yum clean all

RUN ln -f -s /usr/share/zoneinfo/Chile/Continental /etc/localtime
ADD ganglia.conf /etc/httpd/conf.d/ganglia.conf

CMD /etc/init.d/httpd start && /usr/sbin/gmetad -d 1

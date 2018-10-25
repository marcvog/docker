# gmond aggregator
#FROM centos:7
FROM gitlab-registry.cern.ch/atlas-sit/docker/build-athena
MAINTAINER marcvog@uc.cl

USER root
WORKDIR /root

RUN yum install -y ganglia-gmond \
    && yum clean all

CMD /usr/sbin/gmond -f -d 1

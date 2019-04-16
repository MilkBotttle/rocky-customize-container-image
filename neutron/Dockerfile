FROM docker.io/tripleorocky/centos-binary-neutron-server:c9f581caeb51cbdd87f9284176d40bdcca628f56_ad69faca
LABEL maintainer='cameron.c@inwinstack.com'

USER root

RUN yum install -y \
                   python2-mock.noarch \
                   openstack-neutron-fwaas

RUN cp /usr/lib/python2.7/site-packages/neutron_lbaas/extensions/* /usr/lib/python2.7/site-packages/vmware_nsx/extensions/.
USER neutron


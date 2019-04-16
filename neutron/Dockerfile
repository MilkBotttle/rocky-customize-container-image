FROM docker.io/tripleorocky/centos-binary-neutron-server:c9f581caeb51cbdd87f9284176d40bdcca628f56_ad69faca
LABEL maintainer='cameron.c@inwinstack.com'

USER root

RUN yum install -y \
                   python2-mock.noarch \
                   openstack-neutron-fwaas

RUN cp /usr/lib/python2.7/site-packages/neutron_lbaas/extensions/* /usr/lib/python2.7/site-packages/vmware_nsx/extensions/.

RUN echo "[fwaas]" >> /etc/neutron/neutron.conf && \
    echo "enabled=True" >> /etc/neutron/neutron.conf && \
    echo "driver=vmware_nsxv3_edge_v2" >> /etc/neutron/neutron.conf

USER neutron


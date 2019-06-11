FROM docker.io/tripleorocky/centos-binary-neutron-server:current-tripleo
LABEL maintainer='cameron.c@inwinstack.com'

USER root

RUN yum install -y \
                   python2-mock.noarch \
                   openstack-neutron-fwaas

RUN cp /usr/lib/python2.7/site-packages/neutron_lbaas/extensions/* /usr/lib/python2.7/site-packages/vmware_nsx/extensions/.
RUN mkdir /fwaas
RUN crudini --set /fwaas/fwaas_driver.ini fwaas driver vmware_nsxv3_edge_v2 && \
    crudini --set /fwaas/fwaas_driver.ini fwaas enabled True && \
    crudini --set /fwaas/fwaas_driver.ini fwaas agent_version v2

RUN chown -R neutron:neutron /fwaas
USER neutron

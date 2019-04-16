FROM docker.io/tripleorocky/centos-binary-horizon:current-tripleo
LABEL maintainer="cameron.c@inwinstack.com"

RUN yum remove openstack-octavia-ui -y
RUN yum install python-pip -y
RUN pip install neutron-fwaas-dashboard==1.5.0 neutron-vpnaas-dashboard==1.5.0
RUN cp /usr/lib/python2.7/site-packages/neutron_fwaas_dashboard/enabled/_70*_*.py /usr/lib/python2.7/site-packages/openstack_dashboard/local/enabled/


FROM docker.io/tripleorocky/centos-binary-heat-engine:current-tripleo
LABEL maintainer='cameron.c@inwinstack.com'

USER root

RUN sed -i 's/max_microversion = None/max_microversion = "2.1"/g' /usr/lib/python2.7/site-packages/heat/engine/clients/os/nova.py

USER heat


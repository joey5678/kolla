FROM %%KOLLA_NAMESPACE%%/%%KOLLA_PREFIX%%neutron-base
MAINTAINER Kolla Project (https://launchpad.net/kolla)

# Install required packages
RUN yum install -y openstack-neutron \
        openstack-neutron-linuxbridge && yum clean all;

# Add required scripts
ADD ./start.sh /start.sh
ADD ./check.sh /check.sh
ADD ./sudoers.sh /sudoers.sh

# Configure and run the service
CMD ["/start.sh"]

FROM centos
MAINTAINER Justin Phelps <linuturk@onitato.com>

# Set various options
USER root
WORKDIR /root

# Update OS
RUN yum -y upgrade

# Install Ansible
RUN yum groupinstall "Development tools" -y
RUN yum install git python-devel python-setuptools openssl-devel -y
RUN easy_install pip
RUN pip install ansible pyrax
RUN mkdir /etc/ansible
RUN echo 'localhost' > /etc/ansible/hosts
RUN echo '[defaults]' >> /etc/ansible/ansible.cfg
RUN echo -n 'hash_behaviour=merge' >> /etc/ansible/ansible.cfg
RUN ansible --version

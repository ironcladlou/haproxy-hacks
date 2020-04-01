FROM centos:7

RUN yum-config-manager --add-repo http://download.devel.redhat.com/rel-eng/dist-git/rhel/rhpkg.repo
RUN yum -y install rhpkg brewkoji krb5-workstation rpmdevtools

COPY krb5.conf /etc/krb5.conf

WORKDIR /dist-git

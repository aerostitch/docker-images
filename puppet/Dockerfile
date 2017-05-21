####################################
# Docker box used for puppet client
####################################

FROM ubuntu:xenial

Maintainer Joseph Herlant<herlantj@gmail.com>

WORKDIR /root
ENV DEBIAN_FRONTEND "noninteractive"

RUN apt-get update && apt-get dist-upgrade -y -qq
RUN apt-get install wget vim-tiny git -y -qq

RUN . /etc/lsb-release && wget
https://apt.puppetlabs.com/puppetlabs-release-pc1-${DISTRIB_CODENAME}.deb &&
dpkg -i puppetlabs-release-pc1-${DISTRIB_CODENAME}.deb
RUN apt-get update && apt-get install puppet-agent

RUN echo 'PATH="/opt/puppetlabs/puppet/bin/:$PATH"' >> /etc/bash.bashrc
ENTRYPOINT [ "/bin/bash" ]

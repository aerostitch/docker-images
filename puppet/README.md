# docker-puppet
Dockerfile for simple box with only Puppet client install.

The entrypoint defined is bash so you don't need to specify /bin/bash in an
interactive environment.

Usage example:
```
docker run -i -t aerostitch/puppet:xenial
```

# docker-aptly
Dockerfiles for aptly. One version by distributions I use.

To start the Ubuntu Trusty version:
```
docker run -t -i aerostitch/aptly /bin/bash
```

To create a mirror using that:
```
# Once in the container:
# - register the gpg key of the repo you want to mirror (requires wget)
apt-get install -y wget
wget -O - http://archive.ubuntu.com/ubuntu/dists/trusty/Release.gpg | gpg
--no-default-keyring --keyring trustedkeys.gpg --import
aptly mirror create ubuntu-trusty http://archive.ubuntu.com/ trusty
```

To create a new repo,  publish it and serve it:
```
# Once in the container:
aptly repo create -comment="Nightly builds" testing
```

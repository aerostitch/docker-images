## Content

Based on [golang latest](https://hub.docker.com/_/golang/) image.

Additions:
 * vim
 * vim-gocomplete
 * golint
 * gocov

## Usage

An example on how I usually run it.

```
docker run -v ${PWD}:/usr/src/app \
  -v ${HOME}/.bashrc:/root/.bashrc \
  -it aerostitch/golang bash
```

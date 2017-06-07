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
export GITHUB_USER=aerostitch
docker run -v ${PWD}:/go/src/github.com/${GITHUB_USER}/$(basename ${PWD}) \
  -v ${HOME}/.bashrc:/root/.bashrc \
  -it aerostitch/golang bash
```

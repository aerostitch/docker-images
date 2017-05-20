## Content

Based on [python latest](https://hub.docker.com/_/python/) image.

Additions:
 * vim
 * git
 * pylint

## Usage

An example on how I usually run it.

```
docker run -v ${PWD}:/usr/src/app \
  -v ${HOME}/.bashrc:/root/.bashrc \
  -v ${HOME}/.vimrc:/root/.vimrc \
  -v ${HOME}/.vim:/root/.vim \
  -it aerostitch/python bash
```

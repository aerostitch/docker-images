FROM golang:latest

COPY vimrc /root/.vimrc
RUN apt update && apt install -y vim vim-gocomplete

RUN go get -u github.com/golang/lint/golint \
    && go install github.com/golang/lint/golint
RUN go get -u github.com/axw/gocov/gocov \
    && go install github.com/axw/gocov/gocov

WORKDIR /go/src

FROM golang:latest

COPY vimrc /root/.vimrc
RUN apt update && apt install -y vim git curl
RUN mkdir -p ~/.vim/autoload ~/.vim/bundle \
    && curl -LSso ~/.vim/autoload/pathogen.vim https://tpo.pe/pathogen.vim \
    && git clone https://github.com/fatih/vim-go.git ~/.vim/bundle/vim-go

RUN go get -u github.com/golang/lint/golint \
    && go install github.com/golang/lint/golint
RUN go get -u github.com/axw/gocov/gocov \
    && go install github.com/axw/gocov/gocov

WORKDIR /go/src

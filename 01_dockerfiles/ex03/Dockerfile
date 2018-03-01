FROM debian

RUN apt-get update -y && apt-get upgrade -y && \
        apt-get install git -y && \
        apt-get install wget -y

WORKDIR $HOME/local
RUN wget https://storage.googleapis.com/golang/go1.8.linux-amd64.tar.gz
RUN tar -xzvf go1.8.linux-amd64.tar.gz

ENV GOROOT=$HOME/local/go
ENV GOPATH=$HOME/gogs
ENV PATH=$PATH:$GOROOT/bin:$GOPATH/bin
WORKDIR $GOPATH/src/github.com/gogits
RUN go get -u github.com/gogits/gogs

WORKDIR $GOPATH/src/github.com/gogits/gogs
RUN go build

EXPOSE 3000

ENV USER=root

ENTRYPOINT ./gogs web
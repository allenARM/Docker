FROM ubuntu

RUN apt-get update
RUN apt-get install --no-install-recommends build-essential ca-certificates -y
RUN apt-get install nginx -y
RUN apt-get install git -y
RUN apt-get install mariadb-server mariadb-client -y
RUN apt-get install golang-go -y
RUN apt-get install wget -y
RUN service mysql start
RUN echo 'export GOPATH=$HOME/go' >> $HOME/.bashrc
RUN go get -u github.com/gogs/gogs
RUN cd /root/go/src/github.com/gogs/gogs && go build -v -tags 'sqlite'


ENV USER="root"
WORKDIR /root/go/src/github.com/gogs/gogs
EXPOSE 3000:3000
EXPOSE 22:22
USER root
CMD ["./gogs", "web"]

#to build
#docker build -t gitserver .
#to run
#docker run -p 3000:3000 -p 32:22 --name testgit gitserver
#in installation choose SQLite3 && Run user "root"

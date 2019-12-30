FROM golang:latest
USER root

ENV TZ JST-9
ENV TERM xterm
ENV HOSTNAME golang_test

RUN apt-get update
RUN apt-get upgrade
RUN apt-get install -y vim less git

RUN echo "# add" >>/root/.bashrc
RUN echo "alias ll='ls -l'" >>/root/.bashrc
RUN echo "export PS1='\n@\[\e[32m\]golang_test\[\e[0m\] \W # '" >>/root/.bashrc
RUN echo "cd ~/opt" >>/root/.bashrc

# Additional golang libraries
# RUN go get xxxxxxxxxxxxxxxxxxxx
# RUN go get yyyyyyyyyyyyyyyyyyy
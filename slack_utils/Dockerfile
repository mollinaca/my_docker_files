FROM python:3.8
USER root

ENV TZ JST-9
ENV TERM xterm
ENV HOSTNAME ${HOSTNAME}

RUN apt-get update
RUN apt-get upgrade
RUN apt-get install -y vim less git
RUN pip install --upgrade pip
RUN pip install setuptools

RUN echo "# add" >>/root/.bashrc
RUN echo "alias ll='ls -l'" >>/root/.bashrc
RUN echo "export PS1='\n@\[\e[32m\]${HOSTNAME}\[\e[0m\] \W # '" >>/root/.bashrc
RUN echo "cd ~/opt" >>/root/.bashrc

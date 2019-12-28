FROM python:3.4.3
USER root

RUN apt-get update
ENV TZ JST-9
ENV TERM xterm

RUN apt-get install -y vim less git
RUN pip install --upgrade pip
RUN pip install --upgrade setuptools

RUN echo "# add" >>/root/.bashrc
RUN echo "alias ll='ls -l'" >>/root/.bashrc
RUN echo "cd ~/opt" >>/root/.bashrc

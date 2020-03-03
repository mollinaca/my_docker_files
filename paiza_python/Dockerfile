FROM python:3.6.8
USER root

RUN apt-get update
ENV TZ JST-9
ENV TERM xterm
ENV HOSTNAME paiza

RUN apt-get install -y vim less git
RUN pip install --upgrade pip
RUN pip install --upgrade setuptools

RUN echo "# add" >>/root/.bashrc
RUN echo "alias ll='ls -l'" >>/root/.bashrc
RUN echo "export PS1='\n@\[\e[32m\]paiza\[\e[0m\] \W # '" >>/root/.bashrc
RUN echo "cd ~/opt" >>/root/.bashrc

FROM python:3.8.0
USER root

RUN apt-get update
ENV TZ JST-9
ENV TERM xterm
ENV HOSTNAME python380

RUN apt-get install -y vim less git
RUN pip install --upgrade pip
RUN pip install --upgrade setuptools
RUN pip install numpy==1.18.0 scipy==1.4.1 scikit-learn==0.22 numba==0.47.0 networkx==2.4

RUN echo "# add" >>/root/.bashrc
RUN echo "alias ll='ls -l'" >>/root/.bashrc
RUN echo "export PS1='\n@\[\e[32m\]python380\[\e[0m\] \W # '" >>/root/.bashrc
RUN echo "cd ~/opt" >>/root/.bashrc

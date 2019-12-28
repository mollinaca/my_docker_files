FROM centos:7
USER root

RUN yum -y update
ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:ja
ENV LC_ALL ja_JP.UTF-8
ENV TZ JST-9
ENV TERM xterm

RUN yum install -y vim less git
RUN yum install -y instsall gcc gcc-c++ automake libtool cppunit cppunit-devel valgrind gdb strace
RUN localedef -f UTF-8 -i ja_JP ja_JP.UTF-8

RUN echo >>/root/.bashrc
RUN echo "cd ~" >>/root/.bashrc
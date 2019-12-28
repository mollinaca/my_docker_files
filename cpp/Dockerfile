FROM centos:7
USER root

RUN yum -y update
ENV TZ JST-9
ENV TERM xterm

RUN yum install -y vim less git
RUN yum install -y instsall gcc gcc-c++ automake libtool cppunit cppunit-devel valgrind gdb strace

RUN echo >>/root/.bashrc
RUN echo "cd ~" >>/root/.bashrc

FROM ubuntu:18.04

LABEL maintainer="jonatan@cs.ubc.ca"

ARG DEBIAN_FRONTEND=noninteractive

RUN apt update
RUN apt install -y python3 gcc make python3-pip && apt clean
RUN apt install -y python3.8

RUN ln -sf /usr/bin/python3.8 /usr/bin/python3

RUN pip3 install sympy matplotlib

ENV LANG=en_US.UTF-8
ENV LC_LANG=en_US.UTF-8

ENV PYTHONIOENCODING=UTF-8
ENV PYTHONPATH=/cgrader/

RUN groupadd sbuser
RUN useradd -g sbuser sbuser

COPY cgrader /cgrader


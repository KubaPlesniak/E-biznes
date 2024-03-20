FROM ubuntu:22.04

RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y software-properties-common
RUN add-apt-repository ppa:deadsnakes/ppa

RUN env DEBIAN_FRONTEND="noninteractive" apt-get install -y python3.8
RUN apt-get update

RUN update-alternatives --install /usr/bin/python python /usr/bin/python3 10
RUN python3 --version

WORKDIR /app
COPY . /app
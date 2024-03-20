FROM ubuntu:22.04

RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y software-properties-common
RUN apt-get install -y curl unzip zip
RUN add-apt-repository ppa:deadsnakes/ppa

RUN env DEBIAN_FRONTEND="noninteractive" apt-get install -y python3.8
RUN apt-get update

RUN update-alternatives --install /usr/bin/python python /usr/bin/python3 10
RUN python3 --version

RUN add-apt-repository ppa:openjdk-r/ppa
RUN apt-get update
RUN apt-get install -y openjdk-8-jdk

RUN apt-get install -y curl
RUN curl -s https://get.sdkman.io | bash
RUN bash -c "source $HOME/.sdkman/bin/sdkman-init.sh && sdk install kotlin"


WORKDIR /app
COPY . /app
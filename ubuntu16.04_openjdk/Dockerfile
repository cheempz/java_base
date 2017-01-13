FROM ubuntu:16.04

SHELL ["/bin/bash", "-c"]

COPY openjdk-ppa.list /etc/apt/sources/list.d/
RUN apt-get update && apt-get install -y software-properties-common \
    && add-apt-repository ppa:openjdk-r/ppa

RUN apt-get update && apt-get install -y \
    apt-transport-https \
    default-jre-headless \
    openjdk-7-jdk \
    openjdk-8-jdk \
    && rm -rf /var/lib/apt/lists/*

RUN update-alternatives --set java /usr/lib/jvm/java-8-openjdk-amd64/jre/bin/java
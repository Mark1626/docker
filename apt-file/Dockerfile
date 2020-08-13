FROM debian:jessie

MAINTAINER nimalan.m

RUN apt-get update && \
    apt-get install -y apt-file && \
    apt-file update

ENTRYPOINT ["apt-file", "search"]

FROM alpine:3.8

MAINTAINER nimalan.m

RUN apk add --no-cache gnupg1 gcc make && \
  wget http://www.musl-libc.org/releases/musl-1.1.24.tar.gz  && \
  wget http://www.musl-libc.org/releases/musl-1.1.24.tar.gz.asc && \
  wget http://www.musl-libc.org/musl.pub && \
  gpg --import musl.pub && \
  gpg --verify musl-1.1.24.tar.gz.asc && \
  tar -xvf musl-1.1.24.tar.gz && \
  cd musl-1.1.24 && \
  ./configure && \
  make && \
  make install

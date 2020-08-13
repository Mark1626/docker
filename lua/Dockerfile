FROM debian:stretch

MAINTAINER nimalan.m

RUN apt-get update

RUN apt-get install -y git gcc make libc-dev libreadline-dev libncurses-dev wget coreutils unzip

RUN wget http://www.lua.org/ftp/lua-5.1.5.tar.gz && \
    tar zxf lua-5.1.5.tar.gz && \
    rm lua-5.1.5.tar.gz && \
    cd lua-5.1.5 && \
    make linux test && \
    make install && \
    cd .. && rm -rf lua-5.1.5

RUN wget "https://luarocks.org/releases/luarocks-3.0.4.tar.gz" \
    && tar zxpf luarocks-3.0.4.tar.gz

RUN cd "luarocks-3.0.4" \
    && ./configure \
    && make bootstrap 

# RUN groupadd --system --gid 1000 lua \
#    && useradd --system --gid lua --uid 1000 --shell /bin/bash --create-home lua \
#    && chown --recursive lua:lua /home/lua

# ENV PATH="/home/lua/.luarocks/bin:${PATH}"

# USER lua
WORKDIR /home/lua

FROM ubuntu:18.04

RUN apt-get update && apt-get install -y \
    git \
    ruby \
    python3-pip \
    bison \
    flex \
    xmlstarlet

RUN gem install kramdown-rfc2629

RUN pip3 install xml2rfc

RUN git clone https://github.com/fenner/bap.git && \
    cd /bap && \
    ./configure && \
    make

ENV PATH="/bap:${PATH}"

RUN echo $PATH

RUN ls ./bap && pwd

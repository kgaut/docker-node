FROM node:10-alpine

RUN apk add --update \
    python \
    python-dev \
    py-pip \
    build-base \
    git \
    openssh-client \
    optipng \
    autoconf \
    jpeg-dev \
    zlib-dev \
    automake \
    libtool \
    pkgconfig \
    rsync \
    nasm \
  && pip install virtualenv \
  && rm -rf /var/cache/apk/*

RUN npm install -g gulp foundation-cli

WORKDIR /app

RUN npm set progress=false

RUN npm install

FROM node:8-alpine

RUN apk add --update \
    python3 \
    python3-dev \
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
  && pip install virtualenv \
  && rm -rf /var/cache/apk/*

RUN npm install -g gulp

WORKDIR /app

RUN npm set progress=false

RUN npm install

FROM node:13-alpine

RUN apk add --update \
    python \
    python-dev \
    py-pip \
    build-base \
    git \
    openssh-client \
    optipng \
    zlib \
    jpeg-dev \
    zlib-dev \
  && pip install virtualenv \
  && rm -rf /var/cache/apk/*

RUN npm install -g gulp

WORKDIR /app

RUN npm set progress=false

RUN npm install

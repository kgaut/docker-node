FROM node:13-alpine

RUN apk add --update \
    python \
    python-dev \
    py-pip \
    build-base \
    git \
    openssh-client \
    optipng \
  && pip install virtualenv \
  && rm -rf /var/cache/apk/*

RUN apk add jpeg-dev zlib-dev

RUN npm install -g gulp

WORKDIR /app

RUN npm set progress=false

RUN npm install

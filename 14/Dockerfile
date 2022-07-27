FROM node:14-alpine

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
    libpng \
    libpng-dev \
    rsync \
    util-linux \
    vips-dev  \
    dpkg  \
    nasm \
    tiff \
    jpeg \
    pkgconf \
    file \
  && pip install virtualenv \
  && rm -rf /var/cache/apk/*
  
RUN pip install virtualenv

WORKDIR /app

RUN npm set progress=false

RUN npm install -g gulp

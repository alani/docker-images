FROM gliderlabs/alpine:latest
MAINTAINER Ahmed Alani

ENV HUGO_VERSION=0.26
RUN apk add --update \
  wget \
  ca-certificates \
  python \
  python-dev \
  py-pip \
  bash && \
  pip install pygments && \
  wget https://github.com/gohugoio/hugo/releases/download/v${HUGO_VERSION}/hugo_${HUGO_VERSION}_Linux-64bit.tar.gz && \
  tar xzf hugo_${HUGO_VERSION}_Linux-64bit.tar.gz && \
  rm hugo_${HUGO_VERSION}_Linux-64bit.tar.gz && \
  mkdir -p /usr/local/bin && \
  mv hugo /usr/local/bin/hugo

VOLUME /src
WORKDIR /src

ENTRYPOINT ["hugo"]
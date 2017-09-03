FROM anapsix/alpine-java:8_jdk
MAINTAINER Ahmed Alani

RUN apk add --update \
bash \
curl-dev \
ruby \
ruby-dev \
ruby-irb \
ruby-rdoc \
ruby-rake \
ruby-io-console \
ruby-bundler && \
gem install s3_website --no-ri --no-rdoc && \
s3_website install

VOLUME /src
WORKDIR /src

ENTRYPOINT ["s3_website"]
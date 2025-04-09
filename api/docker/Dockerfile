# Few updates made
FROM ruby:2.6.5-alpine
RUN apk update && apk upgrade --no-cache
RUN apk add --no-cache git build-base curl
RUN curl -fsSL https://unofficial-builds.nodejs.org/download/release/v14.17.6/node-v14.17.6-linux-x64-musl.tar.xz -o node.tar.xz && \
    tar -xf node.tar.xz --strip-components=1 -C /usr/local && \
    rm node.tar.xz
RUN npm install -g widdershins && gem install bundler -v 2.4.22
WORKDIR /openapi
RUN git clone https://github.com/slatedocs/slate
WORKDIR /openapi/slate
RUN bundle install
FROM alpine:latest
MAINTAINER Ruben ten Hove <git@rhtenhove.nl>

ARG GOPATH=/

RUN apk --no-cache --update add go git build-base && \

go get -v github.com/spf13/hugo && \

apk del go git build-base

ENTRYPOINT hugo

CMD ["--baseURL=$BASEURL", "--port=80", "--appendPort=false", "--bind=*"]

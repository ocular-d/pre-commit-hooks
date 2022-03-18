FROM alpine:3.15.1
ENV VALE_VERSION=2.15.3

LABEL description="Vale linter"
LABEL maintainer="sven@testthedocs.org"
LABEL name=vale version=${VALE_VERSION}

#RUN apk update && apk add --no-cache wget zip tar
WORKDIR /

RUN apk add --no-cache py3-docutils && \
    addgroup -S vale && adduser -D -S vale vale && \
    wget https://github.com/errata-ai/vale/releases/download/v${VALE_VERSION}/vale_${VALE_VERSION}_Linux_64-bit.tar.gz && \
    tar -xvzf vale_${VALE_VERSION}_Linux_64-bit.tar.gz && \
    cp vale /usr/local/bin/vale && \
    rm README.md && rm LICENSE


CMD [ "/usr/local/bin/vale" ]
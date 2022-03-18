FROM alpine:3.15.1
ENV VALE_VERSION=2.15.3

LABEL description="Vale linter"
LABEL maintainer="sven@testthedocs.org"
LABEL name=vale version=${VALE_VERSION}

#RUN apk update && apk add --no-cache wget zip tar
RUN wget https://github.com/errata-ai/vale/releases/download/v${VALE_VERSION}/vale_${VALE_VERSION}_Linux_64-bit.tar.gz
#RUN wget https://github.com/errata-ai/vale/releases/download/v2.15.3/vale_-bit.tar.gz
#RUN wget https://github.com/errata-ai/vale/releases/download/v2.15.3/vale_2.15.3_Linux_64-bit.tar.gz
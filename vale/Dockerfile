FROM alpine:3.16
ENV VALE_VERSION=2.20.1

LABEL description="Vale linter"
LABEL maintainer="sven@testthedocs.org"
LABEL name=vale version=${VALE_VERSION}

#RUN apk update && apk add --no-cache wget zip tar
WORKDIR /

# hadolint ignore=DL3018
RUN apk add --no-cache py3-docutils bash && \
    addgroup -S vale && adduser -D -S vale vale && \
    wget -nv https://github.com/errata-ai/vale/releases/download/v${VALE_VERSION}/vale_${VALE_VERSION}_Linux_64-bit.tar.gz && \
    tar -xvzf vale_${VALE_VERSION}_Linux_64-bit.tar.gz && \
    cp vale /usr/local/bin/vale && \
    rm README.md && rm LICENSE

#RUN mkdir /src && \
#    chown vale:vale /src


COPY vale.ini src/.vale.ini
COPY styles /styles
WORKDIR /src
COPY --chown=vale:vale vale.ini /src/.vale.ini
#COPY --chown=vale:vale styles /src/styles
USER vale
ENTRYPOINT [ "bash" ]
#ENTRYPOINT [ "/usr/local/bin/vale" ]
#CMD [ "bash", "ls" ]

FROM python:3.9-alpine
ENV version=22.1.0

LABEL description="Black Python code formater"
LABEL maintainer="sven@testthedocs.org"
LABEL name=black version=$version

RUN apk add --no-cache --virtual=.build-deps build-base && \
    addgroup -S black && adduser -D -S black black && \
    pip install --no-cache-dir black==$version && \
    apk del .build-deps && \
    mkdir /src

USER black

CMD ["black"]

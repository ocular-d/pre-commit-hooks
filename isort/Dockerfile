FROM python:3.9-alpine
ENV version=5.7.0

LABEL description="Black Python code formater"
LABEL maintainer="sven@testthedocs.org"
LABEL name=black version=$version

RUN addgroup -S isort && adduser -D -S isort isort && \
    pip install --no-cache-dir isort==$version && \
    mkdir /src

USER isort

CMD ["isort"]

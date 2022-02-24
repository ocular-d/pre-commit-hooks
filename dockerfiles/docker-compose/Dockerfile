FROM python:3.9-alpine
ENV version=1.29.2

LABEL description="Docker Compose validation"
LABEL maintainer="sven@testthedocs.org"

COPY compose_validate.py /usr/local/bin/compose_validate.py

# hadolint ignore=DL3018
RUN apk add --no-cache --virtual=.build-deps build-base libffi-dev && \
    addgroup -S compose && adduser -D -S compose compose && \
    pip install --no-cache-dir docker-compose==$version && \
    chmod +x /usr/local/bin/compose_validate.py && \
    apk del .build-deps libffi-dev && \
    mkdir /src

# hadolint ignore=DL3018
RUN apk add --no-cache bash vim

#USER compose

ENTRYPOINT [ "bash" ]
#CMD ["compose_validate.py"]
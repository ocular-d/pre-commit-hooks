FROM node:lts-alpine3.17
ENV APP_VERSION=6.17.0

LABEL description="TBD"
LABEL maintainer="sven@testthedocs.org"

# hadolint ignore=DL3018
RUN mkdir -p /app \
    && chown -R node:node /app \
    && apk add --no-cache bash \
    && npm install -g cspell@${APP_VERSION} \
    && npm cache clean --force

USER node
#COPY cspell.json /cspell.json
WORKDIR /app
COPY cspell.json cspell.json

WORKDIR /app/spec
#ENTRYPOINT [ "bash" ]
ENTRYPOINT [ "cspell" ]
#CMD ["cspell"]

FROM node:lts-alpine3.17
ENV APP_VERSION=6.6.0

LABEL description="TBD"
LABEL maintainer="sven@testthedocs.org"

# hadolint ignore=DL3018
RUN mkdir -p /app \
    && chown -R node:node /app \
    && apk add --no-cache bash \
    && npm install -g @stoplight/spectral-cli@${APP_VERSION} \
    && npm cache clean --force

USER node
WORKDIR /app

#ENTRYPOINT [ "bash" ]
ENTRYPOINT [ "spectral", "lint" ]

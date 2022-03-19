FROM node:lts-alpine3.15
ENV APP_VERSION=0.31.1

LABEL description="Command Line Interface for Markdown Lint"
LABEL maintainer="sven@testthedocs.org"

# hadolint ignore=DL3018
RUN mkdir -p /app \
    && chown -R node:node /app \
    && apk add --no-cache bash \
    && npm install -g markdownlint-cli@${APP_VERSION} \
    && npm cache clean --force

USER node
WORKDIR /app

#ENTRYPOINT [ "bash" ]
ENTRYPOINT [ "markdownlint" ]
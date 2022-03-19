FROM node:lts-alpine3.15
ENV APP_VERSION=0.31.1

LABEL description="Command Line Interface for Markdown Lint"
LABEL maintainer="sven@testthedocs.org"

RUN mkdir -p /app \
    && chown -R node:node /app \
    && npm install -g markdownlint-cli@${APP_VERSION} \
    && npm cache clean --force

USER node
WORKDIR /app

CMD [ "markdownlint" ]
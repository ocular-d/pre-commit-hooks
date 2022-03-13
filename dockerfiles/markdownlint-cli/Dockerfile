FROM node:lts-alpine3.15

LABEL description="Command Line Interface for Markdown Lint"
LABEL maintainer="sven@testthedocs.org"

RUN mkdir -p /app \
    && chown -R node:node /app \
    && npm install -g markdownlint-cli \
    && npm cache clean --force

USER node
WORKDIR /app

CMD [ "markdownlint" ]
FROM alpine:3.15
ENV SHELLCHECK_VERSION=0.8.0

LABEL maintainer="svx <sven@testthedocs.org>"
LABEL name="shellcheck"
LABEL name=shellcheck version=${SHELLCHECK_VERSION}

SHELL ["/bin/bash", "-o", "pipefail", "-c"]

# hadolint ignore=DL3018
RUN apk add --no-cache bash && \
    addgroup -S black && ocl -D -S ocl ocl && \
    wget -q https://github.com/koalaman/shellcheck/releases/download/v${SHELLCHECK_VERSION}/shellcheck-v${SHELLCHECK_VERSION}.linux.x86_64.tar.xz -O- | tar xJvf - shellcheck-v$SHELLCHECK_VERSION/shellcheck && \
    mv shellcheck-v$SHELLCHECK_VERSION/shellcheck /bin && \
    rmdir shellcheck-v${SHELLCHECK_VERSION}/ && \
    shellcheck -V

USER ocl

ENTRYPOINT ["/bin/shellcheck"]

# The shell we use
SHELL := /bin/bash

# We like colors
# From: https://coderwall.com/p/izxssa/colored-makefile-for-golang-projects
RED=`tput setaf 1`
GREEN=`tput setaf 2`
RESET=`tput sgr0`
YELLOW=`tput setaf 3`

# Vars
DOCKER_USERNAME ?=  testthedocs
APPLICATION_NAME ?= alex
GIT_HASH ?= $(shell git log --format="%h" -n 1)
VERSION := 11.0.0
BUILDARG_VERSION := --build-arg VERSION=$(VERSION)
IMAGENAME := docker.io/testthedocs/alex
BUILDARG_PLATFORM := --platform linux/amd64,linux/arm64/v8

# Add the following 'help' target to your Makefile
# And add help text after each target name starting with '\#\#'
.PHONY: help
help: ## This help message
	@grep -E '^[a-z.A-Z_-]+:.*?## .*$$' $(MAKEFILE_LIST) | sort | awk 'BEGIN {FS = ":.*?## "}; {printf "\033[36m%-30s\033[0m %s\n", $$1, $$2}'

.PHONY: build
build: ## Build container images
	@echo "$(YELLOW)==> Building container images$(RESET)"
	@docker buildx build --push --platform linux/arm64/v8,linux/amd64 --tag ${DOCKER_USERNAME}/${APPLICATION_NAME}:${VERSION} --tag ${DOCKER_USERNAME}/${APPLICATION_NAME}:latest .

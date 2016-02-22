# Scripts to Rule Them All

Based on GitHub [idea](https://github.com/github/scripts-to-rule-them-all). Docker specialized.

This is a boilerplate based on what we use for all our dockerized projects here on Pagar.me.

# Docker

Note that all sample files in this repository are only usable for development and CI contexts and are not suitables for production usage.

# The Scripts

## script/bootstrap

This script installs and builds all dependencies of the project.

This can mean RubyGems, npm packages, Ruby and NodeJS versions and Docker images(as described by docker-compose).

## script/server

Starts the project `web` docker-compose service.

## script/test

Runs all test service instances and runs all tests inside a Docker container.

## script/console

Executes a bash shell inside a container.

## script/run-tests

This scripted is executed by `script/test` inside a container.


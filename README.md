# Scripts to Rule Them All

Based on GitHub [idea](https://github.com/github/scripts-to-rule-them-all). Docker specialized.

This is a boilerplate based on what we use for all our dockerized projects here on Pagar.me.

# Docker

Note that all sample files in this repository are only usable for development and CI contexts and are not suitable for production usage.

# The Scripts

## script/docker-compose-noconflict

This script calls the real `docker-compose` setting the project name accordingly with the current username and build context.

This is useful when running several instances in parallel(i.e.: same CI server).

## script/rebuild

Rebuilds all docker images.

## script/teardown

Destroy all containers, images and volumes created by docker-compose.

## script/cibuild

This is the main script when running tests in the CI. Prepares the build context, bootstraps the project and the calls `script/test`.

## script/bootstrap

This script installs and builds all dependencies of the project.

This can mean RubyGems, npm packages, Ruby and NodeJS versions and Docker images.

## script/test

Runs all test service instances and runs all tests inside a Docker container. Actuallyjust runs `script/run-tests`.

## script/console

Executes a bash shell inside a container.

## script/server

Starts the project `web` docker-compose service.

## script/run-tests

This scripted is executed by `script/test` inside a container.


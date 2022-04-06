This file contains instructions for how to build and update a docker image.

The main purpose of this image is for running composer install on bitbucket pipelines.

Update the commands in the Dockerfile or Ansible then RUN

`docker build -f Dockerfile-8.1 -t bitbucket-composer-8.1 .`
`docker build -f Dockerfile-8.0 -t bitbucket-composer-8.0 .`
`docker build -f Dockerfile-7.4 -t bitbucket-composer-7.4 .`

When you commit to the github repo it will then trigger the image to be rebuilt on github actions and publish to docker hub.

Run the container locally after building.

`docker run -i -t -P lionslair/bitbucket-composer:latest /lib/systemd/systemd`

## URLS
* [bitbucket-composer@dockerhub](https://hub.docker.com/r/lionslair/bitbucket-composerp/)
* [Github repo](https://github.com/lionslair/bitbucket-composer)

## OS image
* Ubuntu 20.04

## packages
* PHP 7.4 | PHP 8.0 | PHP 8.1
* git
* composer

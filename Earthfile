FROM ubuntu:20.10

## for apt to be noninteractive
ENV DEBIAN_FRONTEND noninteractive
ENV DEBCONF_NONINTERACTIVE_SEEN true

RUN apt-get update && apt-get install -y ssh

test:
  RUN echo hello world
  RUN --ssh ssh -o "StrictHostKeyChecking=no" git@github.com

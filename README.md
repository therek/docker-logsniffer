# A Docker container for Logsniffer

[![Docker Automated Build](https://img.shields.io/docker/automated/therek/logsniffer.svg)](https://img.shields.io/docker/automated/therek/logsniffer.svg)
[![Docker Build Status](https://img.shields.io/docker/build/therek/logsniffer.svg)](https://img.shields.io/docker/build/therek/logsniffer.svg)

This repository contains the source for the [Logsniffer](http://www.logsniffer.com/) [Docker](https://www.docker.com) image. It provides a simple image with only Logsniffer installed, leaving proxy and authentication configuration to you.

## Simple usage

To start a new container and bind to host's port 8082:

    docker run -n logsniffer -p 8082:8082 -t therek/logsniffer

## Docker-compose usage

    version: "2"

    services:
      logsniffer:
        image: therek/logsniffer
        ports:
          - 8082:8082
        volumes:
          - /var/log:/mnt/log

## Exposed ports
* 8082

## Volumes
* **/logsniffer**. This is where Logsniffer stores it's files and logs.

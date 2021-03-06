# OpenSMTPD Docker Container Image

[![Build Status](https://travis-ci.org/wodby/opensmtpd.svg?branch=master)](https://travis-ci.org/wodby/opensmptd)
[![Docker Pulls](https://img.shields.io/docker/pulls/wodby/opensmtpd.svg)](https://hub.docker.com/r/wodby/opensmtpd)
[![Docker Stars](https://img.shields.io/docker/stars/wodby/opensmtpd.svg)](https://hub.docker.com/r/wodby/opensmtpd)
[![Docker Layers](https://images.microbadger.com/badges/image/wodby/opensmtpd.svg)](https://microbadger.com/images/wodby/opensmtpd)

## Docker images

❗️For better reliability we release images with stability tags (`wodby/opensmtpd:6-X.X.X`) which correspond to [git tags](https://github.com/wodby/opensmtpd/releases). We strongly recommend using images only with stability tags. 

Overview:

* All images are based on Alpine Linux
* Base image: [wodby/alpine](https://github.com/wodby/alpine)
* [Travis CI builds](https://travis-ci.org/wodby/opensmtpd) 
* [Docker Hub](https://hub.docker.com/r/wodby/opensmtpd)

Supported tags and respective `Dockerfile` links:

* `6`, `6.0`, `latest` [_(Dockerfile)_](https://github.com/wodby/opensmtpd/tree/master/Dockerfile)

## Environment variables

| Variable                     | Default Value | Description |
| ---------------------------- | ------------- | ----------- |
| `OPENSMTPD_BOUNCE_WARN`      | `1h, 6h, 2d`  |             |
| `OPENSMTPD_EXPIRE`           | `4d`          |             |
| `OPENSMTPD_MAX_MESSAGE_SIZE` | `35M`         |             |
| `RELAY_HOST`                 |               |             |
| `RELAY_USER`                 |               |             |
| `RELAY_PASSWORD`             |               |             |
| `RELAY_PORT`                 | `587`         |             |

## Orchestration actions

Usage:
```
make COMMAND [params ...]

commands:
    check-ready [host max_try wait_seconds delay_seconds]
 
default params values:
    host localhost
    max_try 1
    wait_seconds 1
    delay_seconds 0
```

## Deployment

Deploy OpenSMTPD to your own server via [![Wodby](https://www.google.com/s2/favicons?domain=wodby.com) Wodby](https://wodby.com/stacks/opensmtpd).

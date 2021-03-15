# HTTP-FLV

## Introduction

This repo is a Docker image of [nginx-http-flv-module](https://github.com/winshining/nginx-http-flv-module), an updated version of (https://github.com/mugennsou/http-flv) with custom configs for my personal needs

## Installation

Pull Docker image:

```shell
docker pull ssalex/nginx-http-flv
```

Note: you can pull the `ssalex/nginx-http-flv:dev` tag to experience the latest (in developing) nginx-http-module.

## Usage

Start nginx-http-flv server:

```shell
docker run --rm -it -p 7075:7075 -p 1965:1965 ssalex/nginx-http-flv
```

Push RTMP stream to nginx-http-flv server:

```shell
ffmpeg -re -i example.mp4 -vcodec copy -acodec copy -f flv rtmp://127.0.0.1/demo/stream-1
```

You can read here for more details:

[nginx-http-flv-module](https://github.com/winshining/nginx-http-flv-module)

[nginx-rtmp-module](https://github.com/arut/nginx-rtmp-module)

[flv.js](https://github.com/bilibili/flv.js)

[docker-nginx](https://github.com/nginxinc/docker-nginx)

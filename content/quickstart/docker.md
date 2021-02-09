---
title: "Use a Docker image"
description: "Docker images are available for releases, and is a quick way to get up and running."
date: 2020-11-17T20:11:42+01:00
lastmod: 2020-11-17T20:11:42+01:00
draft: false
images: []
weight: 030
toc: false
type: subpages
---

1. Pull the `latest` version [from Dockerhub](https://hub.docker.com/r/gabekangas/owncast/tags): `docker pull gabekangas/owncast:latest`.
1. Run `docker run -p 8080:8080 -p 1935:1935 -it gabekangas/owncast:latest` to start the service.
1. To modify the configuration, you can [take a blueprint from the docs](/docs/configuration/#full-example) and save it to ˋconfig.yamlˋ. Then, bind the file inside docker: ``docker run -v `pwd`/data:/app/data -p 8080:8080 -p 1935:1935 -it gabekangas/owncast:latest``.
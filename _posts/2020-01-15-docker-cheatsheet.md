---
title: "Docker CLI cheatsheet"
layout: post
date: 2020-01-15
image: /assets/images/
headerImage: false
tag:
- Docker
- learning
category: blog
author: naka
description:
hidden: False
---
To help me remember how to wrangle Docker containers. Using the docker image of DeepHLApan from [here](https://github.com/jiujiezz/deephlapan) as an example.

#### to run an image and open a bash shell inside the new container
`docker run -it --rm biopharm/deephlapan:v1.1 bash`

#### to run and image and mount a volume to share files
`docker run --rm -itv"$(pwd)"/local_dir:/path/to/container_dir/ biopharm/deephlapan:v1.1 /bin/bash`

`"$(pwd)"` is to get the current directory

#### to exit docker container but leave it running
Ctrl+P, followed by Ctrl+Q

#### to see running containers
`docker ps`

#### to re-enter a running docker container
`docker exec -it CONTAINER`

`CONTAINER` = a 12-digit alphanumeric or a name like `musing_dubinsky`

#### to copy files into a container
`docker cp path/to/source CONTAINER:/path/to/dest`

#### to copy files out of a container
`docker cp CONTAINER:path/to/source /path/to/dest`

#### to kill a container
`docker kill CONTAINER`

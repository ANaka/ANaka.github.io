---
title: "WSL cheatsheet"
layout: post
date: 2020-02-06
image: /assets/images/
headerImage: false
tag:
- learning
- WSL
- Linux
category: blog
author: naka
description:
hidden: True
---
Because I do this all the time
`sudo mount -t drvfs '\\10.100.104.7\shared' /mnt/r`

Actually, it is smartest to put that line into
`/etc/bash.bashrc`
so that you don't have to do it every time

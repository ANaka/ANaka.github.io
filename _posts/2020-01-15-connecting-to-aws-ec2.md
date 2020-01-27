---
title: "EC2 cheatsheet"
layout: post
date: 2020-01-15
image: /assets/images/
headerImage: false
tag:
- AWS
- EC2
- learning
category: blog
author: naka
description:
hidden: False
---
Some notes here on connecting to EC2 instances. Amazon has a very good
[tutorial](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AccessingInstancesLinux.html)
on this, writing up here just as a cheatsheet since I'm starting to use them a lot lately

### Using bash

#### To ssh into EC2
`ssh -i /path/to/pem_file.pem ec2-user@ec2-01-234-56-789.us-west-1-compute.amazonaws.com`

#### To scp a file to EC2
`scp -i /path/to/pem_file.pem /path/to/source_file ec2-user@ec2-01-234-56-789.us-west-1-compute.amazonaws.com:~/path/to/destination_file`

#### To scp a directory to EC2
`scp -r -i /path/to/pem_file.pem /path/to/source_dir ec2-user@ec2-01-234-56-789.us-west-1-compute.amazonaws.com:~/path/to/destination_dir`

#### If permissions for .pem file are too open
`chmod 400 /path/to/pem_file.pem`

### To set up a jupyter notebook running on EC2

#### on EC2

create password protected jupyter server
`jupyter notebook password`

`cd ~`

`mkdir ssl`

`cd ssl`

`openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout mykey.key -out mycert.pem`

activate jupyter server w SSL certificate
`jupyter notebook --certfile=~/ssl/mycert.pem --keyfile ~/ssl/mykey.key`

#### on unix client (e.g. your laptop)

to forward requests from local port 8889 to port 8888 on EC2 instance
`ssh -i /path/to/pem -N -f -L 8889:localhost:8888 ec2-user@ec2-01-234-56-789.us-west-1-compute.amazonaws.com`

Go to [http://localhost:8889](http://localhost:8889) in browser

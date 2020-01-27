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

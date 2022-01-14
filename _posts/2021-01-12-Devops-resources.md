---
layout:     post
title:     DevOps Resources
subtitle:   BY Guanqiao Huang
date:       2021-01-12
author:     HUANG
header-img: img/post-bg-universe.jpg
catalog: true
tags:
    - DevOps
---
# Ubuntu
## AWS CLI
- Install:
`sudo apt install awscli`
- Check version:
`aws --version`
- [Resource](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html)

## ZSH
- Install:
`sudo apt install zsh`
- Check version:
`zsh --version`
- [Resource](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)

## Docker
- First, update your existing list of packages:

`sudo apt update`
 
- Next, install a few prerequisite packages which let apt use packages over HTTPS:

`sudo apt install apt-transport-https ca-certificates curl software-properties-common`
 
- Then add the GPG key for the official Docker repository to your system:

`curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add-`

- Add the Docker repository to APT sources:
`sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"`

- Make sure you are about to install from the Docker repo instead of the default Ubuntu repo:
`apt-cache policy docker-ce`

- Finally, install Docker:
`sudo apt install docker-ce`

- Docker should now be installed, the daemon started, and the process enabled to start on boot. Check that it’s running:
`sudo systemctl status docker`

- [Reference](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04)

## K6
- Install
```bash
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C5AD17C747E3415A3642D57D77C6C491D6AC1D69
echo "deb https://dl.k6.io/deb stable main" | sudo tee /etc/apt/sources.list.d/k6.list
sudo apt-get update
sudo apt-get install k6
```
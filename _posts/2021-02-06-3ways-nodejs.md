---
layout:     post
title:      Nodejs Introduction
subtitle:   BY Guanqiao Huang
date:       2021-02-06
author:     HUANG
header-img: img/post-bg-universe.jpg
catalog: true
tags:
    - nodejs
---
[Reference](https://phoenixnap.com/kb/update-node-js-version)

# 3 Ways to Update Node.js to Latest Version on Linux Systems
## Option 1: Update Node.js with NVM (Node Version Manager)
1. Start by updating the package repository with the command:
`sudo apt update`

2. Install NVM using the curl command:
`curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash`

Alternatively, you use wget and run the command:
`wget -q0- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash`

3. Close and reopen the terminal for system to recognize the changes or run the command:
`source ~/.bashrc`

5. Then, verify if you have successfully installed NVM:
`nvm --version`

6. Before upgrading Node.js, check which version you have running on the system:
`nvm ls`

7. Now you can check for newly available releases with:
`nvm ls-remotes`

8. To install the latest version, use the nvm command with the specific Node.js version:
`nvm install [version.number]`

## Option 2: Update Node.js with NPM (Node Package Manager)
1. First, clear the npm cache:
`npm cache clean -f`

2. Install n, Node’s version manager:
`npm install -g n`

3. With the n module installed, you can use it to:

Install the latest stable version:
`sudo n stable`

Install the latest release:
`sudo n latest`

Install a specific version:
`sudo n [version.number]`
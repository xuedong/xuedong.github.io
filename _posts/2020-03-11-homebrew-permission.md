---
layout: post
title: Homebrew Permission Issue
date:   2020-03-11 21:36:48
categories: macos
---

I recently encountered the following error when trying to upgrade Homebrew packages on my macOS (High Sierra):

```console
foo@bar:~$ Error: Permission denied @ apply2files - /usr/local/share/ghostscript/9.23/Resource/CIDFSubst/ipaexg.ttf
```

While running Homebrew as root is not supported anymore, we cannot simply use `sudo` to overcome the problem. A simple solution can be modify the user permssions of `/usr/local`, for example as stated [here](https://github.com/Homebrew/homebrew-core/issues/45009), we can apply the following command in your terminal:

`sudo chown -R $(whoami):admin /usr/local/* \
&& sudo chmod -R g+rwx /usr/local/*`

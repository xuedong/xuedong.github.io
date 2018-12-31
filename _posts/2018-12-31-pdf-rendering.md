---
layout: post
title: PDF Rendering Issue after Upgrading to Ubuntu 18.04
date: 2018-12-31 17:09:53
categories: programming
---

After being upgraded from Ubuntu 16.04 to Ubuntu 18.04, my os keeps encountering different issues in particular package dependency problems. One example is the installation of latex/pdf-related applications (e.g. texworks, kile, etc) shown below.

```
The following packages have unmet dependencies:
 libpoppler-qt5-1 : Depends: libpoppler73 (= 0.62.0-2ubuntu2.x) but 0.62.0-2ubuntu2.xx is to be installed
E: Unable to correct problems, you have held broken packages.
```

`libpoppler-qt5-1` is a Qt5-based PDF rendering library. The dependency issue happened here due to the out-of-date package requirement of `libpoppler-qt5-1`, thus we need only to downgrade the `libpoppler73` library (x is the precise version required in the issue report of your os).
`sudo apt install libpoppler73=0.62.0-2ubuntu2.x`
`sudo apt install libpoppler-qt5-1`


Happy new year!!!

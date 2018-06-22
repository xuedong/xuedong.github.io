---
layout: post
title: Programming in C with Jupyter Notebook
date:   2017-12-27 02:32:45
categories: programming
---

Using Jupyter Notebook with a C kernel? That's possible with the <a href="https://github.com/brendan-rius/jupyter-c-kernel">Minimal C Kernel for Jupyter</a>. To make use of it, the best practice for the moment IMHO is to use Docker (as is suggested by the author himself), especially for Windows users. Instructions on how to use C kernel with Docker is on the GitHub page. While there has been a manual installation guide on the page too, there are some issues indeed.

## Manual Installation

Works only on Linux and OS X. Windows is not supported yet. If you want to use this project on Windows, please use Docker.

### Dependencies

-   gcc
-   jupyter
-   python 3
-   pip

### Instructions

-   `sudo pip install jupyter-c-kernel`
-   `sudo install_c_kernel` &lt;- `sudo` is indispensable in some environments
-   `jupyter notebook`. Enjoy!

## Troubleshooting

Above are the instructions from the original installation guide page. It says "Enjoy!", well, not yet. Your code will still not be executable for now. The issue here is when you install with `pip`, it doesn't pull in the `resources/` folder as Docker does (so when you are using Docker, you will not be facing with this issue). The solution is very simple, you just need to download the folder from the repository, then put it into the folder where your jupyter-c-kernel is installed. For example, I am using anaconda, thus put it into `/home/username/anaconda3/lib/python3.6/site-packages/`. Then launch `jupyter notebook`, enjoy!

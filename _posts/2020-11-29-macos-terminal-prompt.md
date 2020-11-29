---
layout: post
title: Colored Prompt and Add Git Branch Names to Terminal under macOS
date:   2020-11-29 14:39:21
categories: programming
---

When you are working with some branch of a Git repository, you may want to show the name of the current branch in your terminal in order to avoid wrong whereabouts of your commits.

In this post, I will show how I use the following instructions to create my personal colored Terminal prompt along with some additional features regarding Git. These instructions are inspired by [Cael Kay-Jackson](https://www.mfitzp.com/article/add-git-branch-name-to-terminal-prompt-mac/). My working OS is macOS High Sierra.

The final output will look like the following:

<img src="/assets/terminal_prompt/color_git.png">

First, we need to create a `.bash_profile` file and a `.bashrc` file under your home path if they do not exist already:
```bash
touch ~/.bash_profile
touch ~/.bashrc
```

Now, add the following instructions to your `.bashrc` to set a color scheme for your Terminal prompt.
```bash
if [ -n "$force_color_prompt" ]; then
	if [ -x /usr/bin/tput ] && tput setaf 1 >&/dev/null; then
		color_prompt=yes
	else
		color_prompt=
	fi
fi

if [ "$color_prompt" = yes ]; then
	PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\] $'
else
	PS1='${debian_chroot:+($debian_chroot)}\u@\h:\w $'
fi
unset color_prompt force_color_prompt
```

Then add the following instructions to your `.bash_profile` to display the Git branch name with red color:

```bash
if [ "${BASH-no}" != "no" ]; then
	[ -r ~/.bashrc ] && . ~/.bashrc
fi

# Git prompt with branch
export PS1="$PS1\[\033[31m\]\$(parse_git_branch)\[\033[00m\] "
```

Here since the `$PS1` variable has already been exported by the `.bashrc` file, we need to append the branch information to it instead of exporting it again. The `\[\033[31m\]` part sets the `\$(parse_git_branch)` to red.

Finally, to make everything function, tap
```console
source ~/.bashrc
source ~/.bash_profile
```
in your Terminal. You can play around with the `$PS1` variable to make your own color scheme or prompt style.

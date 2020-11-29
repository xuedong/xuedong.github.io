---
layout: post
title: Colored Prompt and Add Git Branch Names to Terminal under macOS
date:   2020-11-29 14:39:21
categories: shell
---

When you are working with some branch of a Git repository, you may want to show the name of the current branch in your terminal in order to avoid wrong whereabouts of your commits.

In this post, I will show how I use the following instructions to create my personal colored Terminal prompt along with some additional features regarding Git. These instructions are inspired by [Cael Kay-Jackson](https://www.mfitzp.com/article/add-git-branch-name-to-terminal-prompt-mac/). My working OS is macOS High Sierra.

The final output will look like the following:

<img src="../assets/terminal_prompt/color_git.png">

First, we need to create a `.bash_profile` file in you h

```bash
parse_git_branch() {
	git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}

get_git_root() {
	basename $(git rev-parse --show-toplevel 2> /dev/null) 2> /dev/null
}

update_git_prompt()
{
	GIT_BRANCH=$(parse_git_branch)

	if [ -n "$GIT_BRANCH" ]; then
		GIT_ROOT=$(get_git_root)
		echo -ne "\033]0;$(get_git_root): $(parse_git_branch)\007"
	else
		echo -ne "\033]0;\007"
	fi
}

PROMPT_COMMAND="update_git_prompt; $PROMPT_COMMAND"

# uncomment for a colored prompt, if the terminal has the capability; turned
# off by default to not distract the user: the focus in a terminal window
# should be on the output of commands, not on the prompt
#force_color_prompt=yes

if [ -n "$force_color_prompt" ]; then
	if [ -x /usr/bin/tput ] && tput setaf 1 >&/dev/null; then
		color_prompt=yes
	else
		color_prompt=
	fi
fi

if [ "$color_prompt" = yes ]; then
	PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]'
else
	PS1='${debian_chroot:+($debian_chroot)}\u@\h:\w'
fi
unset color_prompt force_color_prompt
```

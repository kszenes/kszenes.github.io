---
layout: post
title: cheat.sh
date: 2024-10-13
description: The online ressource for quickly getting information on core utilities and languages from anywhere
tags: productivity
# categories: sample-posts
related_posts: false
thumbnail: assets/img/blog/chtsh-logo.png
---

# Introduction

Do you often find yourself forgetting common flags for command line utilities?
Would you like to see if there are certain use cases of command line utilities that you haven't even thought of?
While most programs have extensive documentation in their `man` pages, I think it is fair to say that they are not always the easiest to navigate and can be quite dense.

# cheat.sh

In comes [cheat.sh](https://www.cht.sh) (or `cht.sh` for short), which hosts a community-driven set of cheat sheets for various programming languages, tools and utilities.
The best part is that it is made to work seamlessly from the terminal using the `curl` command which is available on most systems by default.
The `cht.sh` homepage serves as a tutorial on how to use the resource and its capabilities:

```text
$ curl cht.sh
      _                _         _    __
  ___| |__   ___  __ _| |_   ___| |__ \ \      The only cheat sheet you need
 / __| '_ \ / _ \/ _` | __| / __| '_ \ \ \     Unified access to the best
| (__| | | |  __/ (_| | |_ _\__ \ | | |/ /     community driven documentation
 \___|_| |_|\___|\__,_|\__(_)___/_| |_/_/      repositories of the world

+------------------------+ +------------------------+ +------------------------+
| $ curl cheat.sh/ls     | | $ cht.sh btrfs         | | $ cht.sh lua/:learn    |
| $ curl cht.sh/btrfs    | | $ cht.sh tar~list      | | Learn any* programming |
| $ curl cht.sh/tar~list | |                        | | language not leaving   |
| $ curl https://cht.sh  | |                        | | your shell             |
|                        | |                        | | *) any of 60           |
|                        | |                        | |                        |
+-- queries with curl ---+ +- own optional client --+ +- learn, learn, learn! -+
+------------------------+ +------------------------+ +------------------------+
| $ cht.sh go/f<tab><tab>| | $ cht.sh --shell       | | $ cht.sh go zip lists  |
| go/for   go/func       | | cht.sh> help           | | Ask any question using |
| $ cht.sh go/for        | | ...                    | | cht.sh or curl cht.sh: |
| ...                    | |                        | | /go/zip+lists          |
|                        | |                        | | (use /,+ when curling) |
|                        | |                        | |                        |
+---- TAB-completion ----+ +-- interactive shell ---+ +- programming questions-+
+------------------------+ +------------------------+ +------------------------+
| $ curl cht.sh/:help    | | $ vim prg.py           | | $ time curl cht.sh/    |
| see /:help and /:intro | | ...                    | | ...                    |
| for usage information  | | zip lists _            | | real    0m0.075s       |
| and README.md on GitHub| | <leader>KK             | |                        |
| for the details        | |             *awesome*  | |                        |
|            *start here*| |                        | |                        |
+--- self-documented ----+ +- queries from editor! -+ +---- instant answers ---+

[Follow @igor_chubin for updates][github.com/chubin/cheat.sh]
```

## Example with `grep`

For instance, if you want to see which flag to pass to `grep` in order to find all lines which **don't contain** a specific search query, you could consult the cheat sheet for `grep`:

```bash
$ curl cht.sh/grep
# To search a file for a pattern:
grep <pattern> <file>

# To perform a case-insensitive search (with line numbers):
grep -in <pattern> <file>

# To recursively grep for string <pattern> in <dir>:
grep -R <pattern> <dir>

# Read search patterns from a file (one per line):
grep -f <pattern-file> <file>

# Find lines NOT containing pattern:
grep -v <pattern> <file>

# Set how many lines to show before (-B) and after (-A) pattern:
grep -B 3 -A 2 <pattern> <file>

# To grep with regular expressions:
grep "^00" <file>                                               # Match lines starting with 00
grep -E "[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}" <file> # Find IP add

# To find all files that match <pattern> in <dir>
grep -rnw <dir> -e <pattern>

# To exclude grep from your grepped output of ps:
# (Add [] to the first letter. Ex: sshd -> [s]shd)
ps aux | grep '[h]ttpd'

# Colour in red {bash} and keep all other lines
ps aux | grep -E --color 'bash|$'
```

This format of documentation only lists the most common commands and doesn't overwhelm the user with every single available option and flag.
For our example, the fifth line from `cht.sh` tells us that the `-v` flag can be used to find lines which **do not** contain a search pattern.

# Combining it with `fzf`

What would be quite neat is to be able to explore the available cheat sheets and dynamically select the desired one and preview it.
This can be achieved by combining the results from `cht.sh` with the popular [fzf](https://github.com/junegunn/fzf) fuzzy finder command line tool.

{% include video.liquid path="assets/video/blog/chtsh-demo.mp4" class="img-fluid rounded z-depth-1" autoplay=true loop=true controls=true muted=true caption="Demo of cht.sh combined with fzf" %}

First, to obtain all available cheat sheets hosted on `cht.sh`, we can use the `:list` query.
This returns a list of all available cheat sheets which we can then be piped to `fzf` to fuzzy search through the results.
The currently selected item's cheat sheet may be queried from `cht.sh` and displayed in `fzf`'s preview window.

All this can be simply achieved using a short command which I aliased to `chtsh` for convenience:

```bash
alias chtsh="curl -s cht.sh/:list | fzf --preview 'curl -s cht.sh/{}'"
```

Note that the `-s` silences the progress bar of the `curl` command such that it is not overlaid on top of the `fzf` window.
As you can see, the preview window maintains the syntax highlighting from the `curl` command and is fully scrollable.

# `fzf` configuration

`fzf` has a number of customization options that can be used to achieve the desired appearance and workflow.
These configurations can be either passed as flags to the `fzf` command or set globally in the environment variable `FZF_DEFAULT_OPTS`.
I use this variable to set the size of the preview window as well as enable vim keybindings for scrolling the preview window (`<C-u>`: up, `<C-d>`: down, etc.):

```sh
export FZF_DEFAULT_OPTS="--preview-window=right,80%:wrap \
                         --bind ctrl-y:preview-up,ctrl-e:preview-down,\
                                ctrl-u:preview-half-page-up,ctrl-d:preview-half-page-down"
```

# Resource

This post is inspired by ThePrimeagen's great [video](https://www.youtube.com/watch?v=hJzqEAf2U4I) on combining `cht.sh` with `tmux` using a simple script.
Actually, if you are an avid `tmux` user, his scripts can be combined with my command for a truly buttery smooth experience using the `cht.sh` facilities.
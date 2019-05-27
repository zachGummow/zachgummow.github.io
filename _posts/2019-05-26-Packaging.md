---
layout: post
title: Packaging Attempt
---

Today I went over the packaging process with my mentors.

I used my Ubuntu 18.04 VirtualBox to go through the process here: [https://www.freecadweb.org/wiki/GitBuildpackage](https://www.freecadweb.org/wiki/GitBuildpackage)

My mentors told me about dot files, which I understand to be a type of hidden file that contains configuration settings. One of the questions I had was where to put the dotfiles. I found the answer to that:

Dot files should be stored in the home directory.

Once the dot files were in my home directory I used
`gbp buildpackage -us -uc`
to begin the packaging process.

Unfortunately I ran into some errors during this step. After investigating the cause by using
`git-pbuilder login --save-after-login` and `cat /etc/apt/sources.list`
to check my distribution configuration we found that this:

`deb http://mirrors.kernel.org/ubuntu/ bionic main restricted universe multiverse
      #deb-src http://mirrors.kernel.org/ubuntu/ bionic main restricted universe multiverse`

was my sources.list. I needed to be using the Debian unstable distribution. Further attempts to change this file did not succeed.

Eventually, we decided that I should use a Debian Test distribution and set it as the unstable version. I downloaded and set up the virtual machine for my next attempt.
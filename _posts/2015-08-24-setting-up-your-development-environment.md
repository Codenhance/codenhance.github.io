---
layout: post
title:  "Setting up your development environment"
date:   2015-09-22 15:12:07
excerpt: "A little downloading, a little installing, and a little configuring go a long way"
published: true
---

To start coding with Python, all you really need is Python. But if you want to write code collaboratively, deploy code on servers, and take advantage of high performance computing infrastructure, you'll need a few more tools.

## Linux

If you're running Linux, there's not much to do. Just install git and vim with your native package manager. On Ubuntu that looks like

`sudo apt-get install git-core vim`

You can get Anaconda Python <a href="http://continuum.io/downloads#all">here</a>. That's all you have to install, brave Linux user; just skip down to the bottom for some configuration advice.

## Mac OSX

You're also in luck if you have a Mac. OSX comes with vim already installed, so you just need git and Anaconda. First install Homebrew, a command line program for installing other programs. It's like a hacker version of an app store. You can get it <a href="http://brew.sh/">here</a>.

Next use Homebrew to install git:

`brew install git`

Finally, snag a copy of Anaconda Python <a href="http://continuum.io/downloads#all">here</a>. You're almost done! Skip to the bottom and read about configuring your environment, and you'll be ready to go.

## Windows

If you're using Windows, you have a few options. My recommendation is to erase your hard drive and start clean with Linux. It's free and it works great -- try it.

If that isn't an option for you, you can install Linux alongside Windows as a dual boot operating system. This leaves your Windows partition unharmed, but it can be kind of a pain to reboot your computer every time you want to write code.

A third approach is to run <a href="https://www.virtualbox.org/">VirtualBox</a>, a free program that allows you to install another OS *inside* your main OS. Install VirtualBox, then download a Linux distribution and install it as a virtual machine. This is a more complicated option, but it allows you to keep Linux tucked away in a little Windows sandbox. I've created a pre-configured virtual machine you can download if you go this route. Here's the <a href="https://www.dropbox.com/s/6e8vwf4cynmwlvq/UbuntuForPythonProgramming.ova?dl=0">link</a>. (Warning: ~2GB)

Of course, you can always install git, vim, and Anaconda Python directly in Windows. All I can say about that is you're on your own, sorry :(

## Configuring your new software

Anaconda Python comes ready to roll, right out of the box. Git and vim benefit from a bit of preliminary tweaking, though.

To set up git, I recommend following <a href="https://help.github.com/articles/set-up-git/#platform-all">these instructions</a> to permanently store the name and email address associated with your code, and <a href="https://help.github.com/articles/caching-your-github-password-in-git/#platform-all">this guide</a> to caching your GitHub password locally so you won't have to type it over and over once you start cranking out commits.

Vim is extremely configurable. It should work fine without any setup, but if you're feeling ambitious you can install <a href="https://github.com/VundleVim/Vundle.vim">Vundle</a>, a Vim plugin manager. Once it's installed, I recommend installing a tab-completion plugin, like <a href="https://github.com/ervandew/supertab">this one</a>.

That's it, you are ready to code.

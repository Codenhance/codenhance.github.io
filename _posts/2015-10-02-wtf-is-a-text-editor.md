---
layout: post
title:  "WTF is a text editor?"
date:   2015-10-03 15:12:07
excerpt: "It's one of the tools that built this web page. And the Internet."
---

A text editor is a program that runs on your computer that allows you to ... edit text. So WTF is text?

## Text is complicated

This is not a trivial subject. [Here](http://www.joelonsoftware.com/articles/Unicode.html) is the best explanation I've seen; try reading it in a couple of months. For now, just think of "text" or "plain text" as characters you can type with your keyboard, without any fancy formatting.

![Image of plain text typed into a terminal](/assets/this_is_plain_text.gif)

## Text is everywhere

This web page contains fancy formatting -- headers, links, even *stuff like this*. It was written as plain text, though. [Take a look](https://raw.githubusercontent.com/Codenhance/codenhance.github.io/master/_posts/2015-10-02-wtf-is-a-text-editor.md).

In fact, every web page you visit is built with HTML, CSS and JavaScript, which are stored in plain text files. Code written in Python (or other languages) is also just plain text. Genetic sequence data is stored as plain text in FASTA files, and genomic structural annotations are stored as plain text in GFF files.

Even your computer's Preferences are typically stored as plain text, in `config` files that you may be frightened to touch. You shouldn't hesitate, though. Most of the time when you click and select options in a graphical menu, you're just running a program that modifies these files for you. Cut out the middle man! 

## The mighty text editor

For this very purpose, every machine you come across will have some sort of plain text editor installed. On Windows it's Notepad. OSX and Linux machines will usually have a command line text editor called [vi](https://en.wikipedia.org/wiki/Vi) installed. 

All the tutorials on this site use a slightly fancier version of vi called [Vim](http://www.vim.org/about.php). If you've don't have it, [these instructions](/tutorials/2015-08-24-setting-up-your-development-environment.html) will help you install it (along with other essential, free computing tools). If you're new to Vim, [here](/tutorials/2015-08-26-how-to-vim.html) is a guide to getting started.

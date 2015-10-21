---
layout: post
title:  "Getting started with VimGolf"
date:   2015-10-07 15:12:07
excerpt: "A fun, social way to level up your skills with the text editor"
---

[VimGolf](http://vimgolf.com/) is a competitive game that improves your text editing skills. It's a great way to kill five minutes inbetween tasks and offers the promise of some seriously obscure bragging rights.

If you're completely unfamiliar with Vim, go try <a href="http://www.openvim.com/tutorial.html">this online tutorial</a>, or at least play <a href="http://www.vimsnake.com/">Vim Snake</a> or <a href="http://vim-adventures.com/">Vim Adventures</a> to get used to the basic movements. What follows will be a quick walkthrough of installing the necessary programs, creating an account, and submitting your first entry.

## What you need

To play VimGolf, you must have:

- Vim
- Ruby
- A Twitter account

If you don't have Vim installed, please start with [this guide](/2015/09/22/setting-up-your-development-environment.html) to setting up your development environment. You'll also get `git` and Anaconda Python out of the deal.

Installing Ruby might seem like a lot of trouble just to play a game, but the process is pretty painless. In fact, Mac users should already have it installed. To double check, type this into your terminal:

`ruby -v`

If you see a message about what version of Ruby is installed, you're good to go.

On Linux, your package manager should handle it for you. If you have Windows, use [RubyInstaller](http://rubyinstaller.org/).

Finally, VimGolf requires a [Twitter](http://twitter.com) account.

Once you have all the requirements in place, it's time to log in and start playing.

## Install and configure VimGolf

Log in with your Twitter account. You should see a black box in the upper right corner of your screen:

![](/assets/vim_golf_key.png)

Copy the key to your clipboard. Then type the first two commands below it into your terminal. Here's what they do:

`gem install vimgolf`

This uses Ruby's package manager to install the VimGolf program on your machine.

`vimgolf setup`

This lets you save your key so the VimGolf program can handle submitting your entries. Here's what the setup screen looks like:

![](/assets/vim_golf_setup.png)

Paste in your key and you're ready to go.

## Your first round of VimGolf

Now it's time to browse the site and pick a challenge. I started with [this one](http://vimgolf.com/challenges/55bcdc3ef4219f456102374f).

Each challenge consists of "before" and "after" text, and your task is to convert the former into the latter using the fewest possible keystrokes. Luckily you can see other peoples' submissions, so it's okay if you're not sure how to start. Just open up Vim, type or paste in the "before" text, press `<esc>` and then type another entry, keystroke for keystroke. *Copying other people's entries is the best way to pick up new Vim tricks and techniques.*

As an example, my Vim challenge was to convert 

> The quick brown fox jumps over the lazy dog.

to 

> The quick lazy dog jumps over the brown fox.

The topmost solution on the page looked like this:

> 2wd2w3wPd3w6bepZZ

So I opened Vim, typed in the "before" text, pressed `<esc>` to exit Insert mode and `gg` to go to the beginning of the file, then typed `2wd2w3wPd3w6bepZZ`. It worked! But how?

It's useful to break VimGolf solutions up into pieces. Here is a breakdown of the seventeen keystrokes above:

`2w` -- Move forward two words

`d2w` -- Delete two words

`3w` -- Move forward three words

`P` -- Paste/put the previously deleted text before the cursor position

`d3w` -- Delete three words

`6b` -- Move back six words

`e` -- Move to the end of the current word

`p` -- Past/put the previously deleted text after the cursor position

`ZZ` -- Save and quit

After a couple of tries, I understood the solution. However, VimGolf requires you to match or beat the solutions you see. So I came up with my own: `2wd2w3wPd3wFkpZZ`. Only 16 keystrokes! The only difference is the use of `Fk` (Move backwards to the nearest occurrence of the letter 'k') instead of `6b` and `e`. One stroke is all it takes, though.

To submit my answer, I typed the following:

`vimgolf put 55bcdc3ef4219f456102374f`

I copied the "55bcd..." part from the black box on the VimGolf web page corresponding to the challenge. Here's what the `vimgolf` program looks like in action:

<div class="text-center">
<img src="/assets/vim_golf_demo.gif">
</div>

---
layout: post
title:  "Clone and run your first program"
date:   2015-09-22 15:12:07
excerpt: "Use git and the command line interface to start running Python programs"
---

(This tutorial assumes you've installed Python and git.)

In less than ten minutes you'll clone a remote repository from the command line and run a simple interactive Python program. Then you can go tell your friends all about it. They will be enthralled.

First take a look at the <a href="https://github.com/Codenhance/boot_camp">repository</a> we're going to clone. That enticing script entitled "reverse_complement.py" is the one we're going to run.

To get this code from GitHub onto your machine, just type this command:

`git clone https://github.com/Codenhance/boot_camp.git`

Easy enough, but where exactly did that URL come from? If you look closely at the above link, you'll find it in a box on the right hand side. It looks like this:

![](/assets/github_clone_url.png)

The above command will download the repository into a folder called 'boot_camp' inside of your current working directory. Enter the repository like this:

`cd boot_camp`

Now run the reverse complement script:

`python reverse_complement.py`

And that's it! You can reverse complement genetic sequences to your heart's content. Here's what the process looked like on my machine:

![](/assets/clone_and_run_reverse_complement.png)

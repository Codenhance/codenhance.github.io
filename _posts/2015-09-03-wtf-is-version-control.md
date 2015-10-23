---
layout: post
title:  "WTF is version control?"
date:   2015-09-22 15:12:07
excerpt: "You need it, you love it, you just might not know it yet"
---

Version control is just a program, like git, that runs on your computer. It allows you to save versions of your code without renaming or copying files and making a mess.

<div class="text-center">
<img src="/assets/files_that_need_version_control.png" title="Don't do this" alt="Image of a disorganized folder full of similarly-named files">
</div>

## Who Cares?

I’m sure you are brilliant, but you are not likely to produce one or ten thousand lines of working code in a sitting. Ever. What you’ll do instead, because you’re brilliant, is start by building the smallest working program you possibly can. You’ll confirm that it works, then you’ll add to it a tiny bit and confirm that it still works. You’ll repeat this process until your program ends hunger and cures diseases.

I left something out, actually. Another thing you’ll do quite often is add a tiny bit to your program and find that YOU COMPLETELY RUINED EVERYTHING. Version control takes all the panic and self loathing out of moments like that. It allows you to roll back to the last working version of your code and start again.

## What Exactly Does it Do?

Here are a few actions you can perform with git, plus the associated commands:

- Keep an eye on this directory - there's code in here and I don’t want to mess anything up -- `git init`
- Make this file part of the next save -- `git add <filename>`
- Save the current state of my project so I can come back to it (or publish it) -- `git commit -m <message>`
- I messed up on this file; revert it back to my last saved version -- `git checkout <filename>`

Git can also handle code that’s hosted remotely, for example on GitHub:

- Pull down some code from online -- `git clone <url-to-git-repository>`
- Update the online version of my project -- `git push origin master`

There's more to git, but you can get a lot of mileage out of the commands listed above. If you want to level up your git skills, here a basic tutorial from [CodeSchool](https://try.github.io/levels/1/challenges/1), and a more advanced one from [pcottle](http://pcottle.github.io/learnGitBranching/).

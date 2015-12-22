---
layout: post
title:  "Python for Scientists"
date:   2015-12-16 15:12:07
---

Spoiler alert: in this post, I will argue that Python is the best programming language for scientists to learn. Forget Perl, Java, FORTRAN, IDL, or whatever else they were pushing when you got your degree. This type of discussion is usually emotionally charged -- many a flame war has been fought over programming languages. Feelings will get hurt. Heads will roll. But first ...

## Do scientists even need to learn to program?

No. Not necessarily. As counseled by Jeff Atwood in ["Please Don't Learn to Code"](http://blog.codinghorror.com/please-dont-learn-to-code/), it's better to focus on solutions rather than methods. A scientist who already has a love-hate-but-mostly-hate relationship with computers would do better to leave the programming to the programmers. This way, the code gets written, the research gets completed, and the scientist herself never has to debug a single syntax error. 

That said, scientists who *are* prepared and motivated to add programming to their skillset couldn't ask for a better language than Python. This post will outline some of the advantages of learning Python and some resources for getting started. But first ...

## Does it even matter what language you learn? 

No. Not necessarily. Most experienced programmers are proficient in several languages, and are able to become productive in a new language over the course of a long weekend. Obviously there's more to learning programming than memorizing the syntax of a single language. That said, Python offers a number of distinct advantage to the beginner.

## The universe wants you to learn Python

One of the greatest strengths of Python is the vibrant community and wealth of high quality training materials available. Want to try Python out without installing anything, just to get a feel for it? [Codecademy](https://www.codecademy.com/learn/python) has you covered. Would you rather watch video lectures and follow a semester format? [Coursera](https://www.coursera.org/learn/python) has a free course that lets you do just that.

Suppose you're more of a textbook learner. You've got a ton of options, including:

- [Learn Python the Hard Way](http://learnpythonthehardway.org/), which takes you from zero to the beginnings of a web game
- [Python for Informatics](http://pythonlearn.com/book.php), which takes beginners all the way to topics like using databases and visualizing data
- [Automate the Boring Stuff with Python](https://automatetheboringstuff.com/), which focuses on the kind of practical, repetitive tasks that scientific computing so frequently requires
- [Intermediate Python](http://book.pythontips.com/en/latest/), a great resource for anyone who's ready to move past the basics and learn some of Python's more powerful features

Even better, all of these texts are free to read online.

## The universe wants you to be productive in Python

It's not just the learning materials that make Python such a great choice for scientists learning to code. There's also a wealth of free packages, tools, and documentation for every field of science you can imagine.

For astronomers, there's Astropy, which contains modules for astronomical [constants](http://docs.astropy.org/en/stable/constants/index.html), [coordinate systems](http://docs.astropy.org/en/stable/coordinates/index.html), [model fitting](http://docs.astropy.org/en/stable/modeling/index.html), and more. Each of the preceding links points to a page with sample code that even a novice can follow in order to get familiar with the package.

For biologists, there's [Biopython](http://biopython.org/wiki/Biopython). Want to [read genetic sequence data](http://biopython.org/DIST/docs/tutorial/Tutorial.html#htoc48)? [Parse BLAST output](http://biopython.org/DIST/docs/tutorial/Tutorial.html#htoc85)? [Read from a protein database](http://biopython.org/DIST/docs/tutorial/Tutorial.html#htoc135)? [Produce a random genome](http://biopython.org/DIST/docs/tutorial/Tutorial.html#htoc281)? Biopython's got you covered.

There are also a number of tools that are useful for all scientists, regardless of their specific field. Machine learning touches nearly every data-driven scientific discipline, and of course you can do it with Python -- just take a look at the beautiful documentation for the [scikit-learn](http://biopython.org/DIST/docs/tutorial/Tutorial.html#htoc281) package. Need to produce publication-quality visualizations? You're guaranteed to find a walkthrough for the chart you need in the thoroughly-documented [Bokeh](http://bokeh.pydata.org/en/latest/) library.

## The universe will thank you for using Python

Python is an open source language*, and so are the libraries mentioned above. As a scientist, this should matter to you. Using open source tools that are widely available is a great way to ensure that your experiments are easily reproducible.

Compare this with the experience of a researcher who would like to extend your experiment, but must first purchase an expensive license in order to recreate your programming environment. This is exactly the case in much of astronomy, with many legacy projects locked into the proprietary IDL language. Working astronomers are largely migrating to Python in order to facilitate collaboration. It's the future!

## Everyone else is doing it

Python's already in use at Google, NASA, the National Weather Service, even the Los Alamos National Laboratory (LANL) Theoretical Physics Division (longer list [here](https://wiki.python.org/moin/OrganizationsUsingPython)). Not to mention nearly a million projects on [GitHub](https://github.com/search?utf8=%E2%9C%93&q=language%3APython&type=Repositories&ref=advsearch&l=Python&l=). This means that the strengths mentioned above -- the high quality training materials, useful libraries, and active community -- will only grow with time. By embracing Python, a scientist enters into a movement toward openness and simplicity in computational science that is already changing the world around us. If you're a scientist looking to learn how to code, I'd love to hear from you in the comments. What's the nature of your research? What will learning Python allow you to do? How can I help you get started?

*Technically an open source _implementation_ of a language.

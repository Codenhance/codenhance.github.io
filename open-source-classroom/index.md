---
layout: post
title:  "The Open Source Classroom"
date:   2015-12-16 15:12:07
---

I completed a Master's degree in Information and Computer Science last summer, and started teaching my first university class (Python Programming) about two weeks later. I'm a self-taught programmer who mostly learned on the job. I've never taken a Python class. To add to the fun, my students ranged from true beginners who had never written a line of code to experienced programmers looking to try out a new language. By rights I should have been doomed from the start.

## Open source saved my life

Despite the challenges presented by my students' diversity of experience and interests, we managed to get through the semester with a minimum of soul-crushing boredom, and several students even learned some Python along the way. This was facilitated entirely by the wealth of open source educational materials and tools available in the Python universe. 

Instead of forcing students to spend $150 on a dry textbook and type through examples that confuse half of the class while boring the other half to tears, I was able to lift the textbook requirement entirely. Instead of one overpriced book, the class used several high-quality, up-to-date, *free* books. Instead of trudging through the same old "implement a linked list" or "build a library lending app" examples that so failed to inspire me during my own education, I was able to assign students tasks like "simulate a galaxy," "design primers for a biological experiment," "make a platformer video game," or "build a web service."

## Open source textbooks

Help for the beginners in the class came in the form of Charles Severance's [Python for Informatics](http://www.pythonlearn.com/html-270/) book (CC BY-NC-SA 3.0). This is the same textbook used in Coursera's "Programming for Everybody" course. Not every student needed such a gentle introduction to the language, and I offered points to any student who typed the code examples from the book and blogged about what they learned.

More experienced programmers who wanted a different kind of introduction to Python were able to jump right in to game programming thanks to the GPL-licensed [Pygame](http://www.pygame.org) module and Al Sweigart's textbook [Invent Your Own Computer Games with Python](http://inventwithpython.com/chapters/) (CC BY-NC-SA 3.0). The students who opted for this approach got points for typing example code from the textbook, and eventually learned to modify the code to create their own games.

## Open source libraries and docs

For true beginners, following the first several chapters of a textbook is sufficient for a semester's work. But what about those experienced programmers who signed up for an easy A? The open source community provided a ton of fun for them, too.

One of Python's greatest strengths as a language is the variety of robust, well supported, thoroughly documented libraries and packages available. For the students who had no need to learn about lists and functions, there was no end to the projects available.

For the science majors, there are several options, including the following BSD-licensed packages:

- [Astropy](http://www.astropy.org/), which contains modules (and sample code) for astronomical [constants](http://docs.astropy.org/en/stable/constants/index.html), [coordinate systems](http://docs.astropy.org/en/stable/coordinates/index.html), [model fitting](http://docs.astropy.org/en/stable/modeling/index.html), and more. 
- [Bokeh](http://bokeh.pydata.org/en/latest/), a visualization library. The documentation is extensive (and beautiful). Any scientist or science major should be able to acquire some interesting test data in her field, and if she can do that, she can turn it into a gorgeous graph just by following the Bokeh examples.
- [Vispy](http://vispy.org/), yet another visualization library which ships with a number of complex, impressive example projects. One beginner was able to find, run, read, comprehend and successfully modify a 3D spiral galazy simulation. How many of you did something that cool in your first semester coding?

While the scientists crunched data in one corner, a number of students interested in learning about web technologies were able to build their own relevant projects, thanks to these great resources:

- [BeautifulSoup](http://www.crummy.com/software/BeautifulSoup/bs4/doc/) is an MIT-licensed package that makes parsing HTML as enjoyable as browsing the rendered version. The docs are a great introduction to Python, parsing, and HTML all in one stop.
- [Flask](http://flask.pocoo.org/docs/0.10/tutorial/) is a BSD-licensed web microframework. The quick, to-the-point tutorial takes newcomers through topics such as templates, requests and responses, database operations and testing. For the intermediate programmer, this single walkthrough is a more complete and engaging introduction to Python than any beginner textbook could offer.

## Games and interactive tutorials

The class also benefited from the plentiful gamified resources available to students of Python and programming in general. Here are a couple of Creative Commons-licensed options:

- [Project Euler](https://projecteuler.net/) is a website with coding challenges that increase in difficulty. They're mostly short, mathematical in nature, and perfect for practicing a new language. Students were able to complete a set of these problems and present their solution in class for points.
- [Slice Like a Ninja](http://bruab.github.io/slice_like_a_ninja/) is a web game I built that presents players with strings and a terminal. The objective is to use Python slice syntax to convert the input string into a given output string. Rather than present a chapter and a test on slices, I waited until students encountered a problem that could be solved with slices, introduced the topic, then sent them to play this game.

Python doesn't happen in a vacuum, and familiarity with the programming environment itself is often the biggest impediment for beginning coders. Some students walked into my class as established command line and version control wizards, but the majority needed onboarding. Here are some amazing (MIT-licensed) resources for learning the command line and related tools:

- [Bashy](http://playbashy.com/) is a short game that introduces basic command line usage while providing visual feedback for those who are having a hard time breaking away from GUI-land. (Full disclosure: I built Bashy in grad school. I don't make money from it though :)
- [OpenVim](http://www.openvim.com/tutorial.html) is an interactive tutorial for complete beginners to the powerful Vim text editor.
- [VimGolf](http://vimgolf.com/) is a command line tool and website which implements a competitive game that helps Vim users of all levels improve their efficiency.
- [learnGitBranching](http://pcottle.github.io/learnGitBranching/) is a rich, thorough, interactive web app that covers beginning and intermediate git commands with beautiful visualizations and encouraging feedback. I refuse to teach programming without requiring version control, so this was a priceless resource. It beats lecturing for hours on end about git!

## Results

The open source classroom achieved mixed results. For more advanced students, it was a huge success. They generally appreciated the opportunity to explore their own interests rather than being tied to the examples in a single textbook, and felt as though they received a solid introduction to Python. Beginners were less enthusiastic, in some cases complaining of feeling overwhelmed or confused. 

In the future, I may attempt to identify students incapable of self-directed study so I can simply push them through a single textbook. However, I think that feeling overwhelmed and confused is a natural response to entering into a world as diverse, rich, and full of possibility as the open source Python universe. It *is* overwhelming to think that there are nearly a million Python projects on [GitHub](https://github.com/search?utf8=%E2%9C%93&q=language%3APython&type=Repositories&ref=advsearch&l=Python&l=), and it's a bit confusing to think that one language can power websites, games, and spaceships. 

Making sense of the open source landscape may simply require more than a semester's worth of effort, but I think every student left with a clear idea of just how many resources are out there, and how much power they offer us.

---
layout: post
title:  "WTF is if __name__ == '__main__'?"
date:   2015-10-20 03:31:00
excerpt: "TL;DR it makes your script run, which is hopefully what you want"
---

You've started reading, running, and even writing Python scripts. Maybe you are so smart that you understand 50-60% of the code you're looking at. That's great! At the *very bottom* of many scripts, though, lurks the cruftiest of code blocks:

{% highlight python %}
if __name__ == '__main__':
    main()
{% endhighlight %}

Wow, seriously? Double underscores? Can it get any uglier or more obscure? Not to worry; this post will move that gibberish from "WTF"-land to "Oh, of course"-ville.

## The short version

That weird and off-putting code basically says "If somebody is running this program from the command line, just execute the `main()` function." Put it in any script you'll want to run as a standalone utility. (Of course, your script also needs a `main()` function for this to work.)

## The long version

Every `.py` file is a [module](http://codenhance.com/2015/10/12/python-modules-and-packages.html). When you run a program with a command like `python my_program.py`, the Python interpreter considers `my_program` to be the "main" module, and will signify this by setting the module's `__name__` variable to have the value `'__main__'` (that's a string). 

This variable starts and ends with double underscores, which marks it as a "magic" attribute (see [here](https://www.python.org/dev/peps/pep-0008/#descriptive-naming-styles)). You can think of this as a meta-variable -- it's not part of your code, it's *about* your code.

The alternate possibility is that the interpreter is reading a module that *isn't* the main module -- for example, when it reads a module that's *imported* by the main module. In these cases, the `__name__` variable is set to the module name itself. So the `if` statement will be `False`, and the `main()` function will never execute.

## A quick example

To see `__name__` in action, create a tiny module with a `main()` function that just prints the module's own `__name__` variable, then run it from the command line:

<div class="text-center">
<img src="/assets/create-a-main-module.gif">
</div>

<hr />

Next, create an equally tiny module that imports your first module and calls that same `main()` function:

<div class="text-center">
<img src="/assets/create-a-module-that-imports.gif">
</div>

<hr />

So when you run `foo.py` from the command line, its `__name__` is `'__main__'`. When you import it, its `__name__` is simply `foo`. If all that's too much to take in, just absorb the short version and keep coding :)

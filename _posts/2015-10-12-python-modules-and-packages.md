---
layout: post
title:  "Python modules and packages"
date:   2015-10-12 08:55:00
excerpt: "A quick tutorial on creating your first example of each"
---

Python modules and packages can be confusing or intimidating at first. This post aims to demystify them once and for all by having you create your *own* working Python package and modules in under twenty minutes.

## Terminology

A Python *module* is just any old `.py` file containing *definitions* and *statements*. You'll create two modules, one with a single definition and one with a single statement.

A *package* is just a way of organizing modules into folders, and importing them as *dotted paths*. We'll see how this works as well.

Here are the [official docs](https://docs.python.org/2/tutorial/modules.html) if you'd like to know more.

<hr />

## Step 1 - Your first Python module

Create a directory to hold our entire package, then navigate inside. Create a file called `my_module.py` and define a trivial function.

<div class="text-center">
<img src="/assets/python_modules/1-create-package-and-module.gif">
</div>

<hr />

## Step 2 - Import and run your code

From inside the same directory as your module, test out different ways of importing and running your function. (You can import the module and use a dotted path to access the function, or you can import the function directly. You can use `python -c` to execute a command, or use the `python` interpreter if you prefer.)

<div class="text-center">
<img src="/assets/python_modules/2-import-and-execute-function.gif">
</div>

<hr />

You can even write a script that imports your function.

<div class="text-center">
<img src="/assets/python_modules/3-write-and-run-a-script.gif">
</div>

<hr />

## Step 3 - Create a submodule

Now make a new directory inside your package directory. Create another module there, this one containing only an assignment statement.

<div class="text-center">
<img src="/assets/python_modules/4-create-submodule.gif">
</div>

<hr />

## Step 4 - Get an ImportError

Try importing your submodule using a dotted path. It doesn't work!

<div class="text-center">
<img src="/assets/python_modules/5-get-an-import-error.gif">
</div>

<hr />

## Step 5 - Add __init__.py

The command line program `touch` creates empty files. Use it to make a file called `__init__.py` in your submodule directory. Now the import works!

<div class="text-center">
<img src="/assets/python_modules/6-add-init-py-to-fix-it.gif">
</div>

<hr />

## That's it

You just made a Python package containing two modules. They don't do much, but the way they are laid out and imported is no different from any other package you'll come across.

## Final challenge

Navigate up one directory -- to the folder containing your package. Try importing `my_module` from here. Why doesn't it work? Can you fix it?

<div class="text-center">
<img src="/assets/python_modules/7-error-importing-package.gif">
</div>

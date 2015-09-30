---
layout: post
title:  "Build a FASTA suite - Part 1/4"
date:   2015-09-29 15:27:07
excerpt: "Set up a new Python project and start reading FASTA files"
---

If you know how to:

- Open a Python script/program in a text editor
- Run a Python script/program from the command line

then this series is for you. Over the course of four posts, we'll build a suite of tools to analyze, modify, and visualize genetic sequence data. Today we'll set up our project, generate some sample data, and write a script to analyze nucleotide distribution. Let's get going.

## Create a new Python project

This is a step that trips up many an inexperienced programmer. It's actually so easy you'll soon be deeply ashamed for thinking it was some kind of big deal. A Python program is just a directory with some `.py` files inside. To make one called "fasta_suite", just type the following in a [terminal](/tutorials/2015-08-31-wtf-is-the-command-line.html):

{% highlight python %}
mkdir fasta_suite
{% endhighlight %}

That's it. Navigate into your new project:

{% highlight python %}
cd fasta_suite/
{% endhighlight %}

There's nothing in here yet. Let's create a new file, make it executable, and open it for editing in Vim:

{% highlight python %}
touch nucleotide_distribution.py
chmod +x nucleotide_distribution.py
vim nucleotide_distribution.py
{% endhighlight %}

## Start with a trivial script

For now let's just make this script take a FASTA file as an argument and print its contents. That might sound trivial, but there are plenty of things that can go wrong along the way. It's best to set a clear, simple goal and work toward it.

{% highlight python linenos %}
#!/usr/bin/env python

import sys

with open(sys.argv[1], 'r') as fasta:
    for line in fasta:
        sys.stderr.write(line)
{% endhighlight %}

## Make some test data

At this point we should stop and test out our script. Except we don't have a FASTA file to feed it. Let's create one:

{% highlight python %}
mkdir data
vim data/two_seqs.fasta
{% endhighlight %}

Edit the newly-created `two_seqs.fasta` so that it lives up to its name:
{% highlight python linenos %}
>seq_foo
GATTACA
>seq_bar
ACGTTGCA
{% endhighlight %}

## Run it

We can now try out our script:

{% highlight python %}
python nucleotide_distribution.py data/two_seqs.fasta
{% endhighlight %}

You should see the contents of the file. Not too exciting, but decent progress. 

## Save it

To celebrate the first successful run of our script, let's officially declare this project underway by bringing it under version control:

{% highlight python %}
git init
git add .
git commit -m "initial commit"
{% endhighlight %}

Now if we make a mess in the steps to come, we can always jump back to this starting point.

## Improve it

It's time to make `nucleotide_distribution.py` live up to its name. The script is already reading the file line by line. We'd like it to count the number of A's, C's, G's and T's on each line, then print a summary of the totals. We can start by adding variables to hold each of these values:

{% highlight python linenos %}
#!/usr/bin/env python

import sys

a_count = 0
c_count = 0
g_count = 0
t_count = 0
with open(sys.argv[1], 'r') as fasta:
    for line in fasta:
        sys.stderr.write(line)
{% endhighlight %}

## Run it again

You should try executing the script again:

{% highlight python %}
python nucleotide_distribution.py data/two_seqs.fasta
{% endhighlight %}

The output hasn't changed, but if you made any typos you'll probably get a Syntax Error. Once things are running smoothly, we can start doing something with those variables. 

## Make the script do stuff

We'll loop over each line, character by character, and check its value. If it's an "A", we'll increment the `a_count` variable. If it's a "C", ... you probably already know what's coming. As one final improvement, we'll print the values of these four variables at the end of the program.

{% highlight python linenos %}
#!/usr/bin/env python

import sys

a_count = 0
c_count = 0
g_count = 0
t_count = 0
with open(sys.argv[1], 'r') as fasta:
    for line in fasta:
    	for character in line:
	    if character == "A":
	        a_count += 1
	    if character == "C":
	        c_count += 1
	    if character == "G":
	        g_count += 1
	    if character == "T":
	        t_count += 1
        sys.stderr.write(line)

print("A: %d" % a_count)
print("C: %d" % c_count)
print("G: %d" % g_count)
print("T: %d" % t_count)
{% endhighlight %}

Run this program with `data/two_seqs.py` and you should get output like this:


{% highlight python %}
A: 5
C: 3
G: 3
T: 4
{% endhighlight %}

## Save it

Congratulations, `nucleotide_distribution.py` now does what it advertises. Another celebration is in order:

{% highlight python %}
git add nucleotide_distribution.py
git commit -m "print nucleotide counts"
{% endhighlight %}

## Wrap up

If you're thinking our script could be better, you're certainly right. In the next post we'll produce some data that breaks `nucleotide_distribution.py` and figure out how to make it stop breaking. We'll also incorporate some built in functions from the Python standard library to make our code more readable. See you there!

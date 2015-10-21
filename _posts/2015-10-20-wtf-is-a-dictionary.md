---
layout: post
title:  "WTF is a dictionary?"
date:   2015-10-20 02:10:00
excerpt: "Spoiler: one of your two favorite Python data structures"
---

A dictionary is a built-in data type in Python. You will use them all the time. Here is the [official documentation](https://docs.python.org/2/tutorial/datastructures.html#dictionaries) -- it's more readable than you might expect. 

If you're familiar with other languages, you can think of a dictionary as resembling a Map or a HashMap. But even if you've never heard any of these words before, this post will get you started with using dictionaries to store and retrieve biological data.

## Keys and Values

Dictionaries "map" keys to values. It's perfectly fine if the preceding sentence means absolutely nothing to you -- after seeing some examples you will develop your instincts for deciding when your data belongs in a dictionary.

Suppose you are working with sequence data. Each entry consists of a header (or name) and a sequence (series of nucleotides). You could store this data in a dictionary! The headers would be keys and the nucleotide strings would be values. When you want to access the sequence corresponding to a certain header, you present that header to the dictionary and it returns the sequence to you. 

Here's a small example. Start up a Python interpreter (just type `python` and press enter). Then type the commands that follow the `>>> ` prompt. 

Create an empty dictionary:

~~~
>>> my_seqs = {}
~~~

Now add a key/value pair to it:

~~~
>>> my_seqs['seq_1'] = 'GATTACA'
~~~

Add another:

~~~
>>> my_seqs['seq_2'] = 'ACTACTACT'
~~~

Now print the dictionary to see what it looks like[*](#1):

~~~
>>> print(my_seqs)
{'seq_1': 'GATTACA', 'seq_2': 'ACTACTACT'}
~~~

What was that first sequence again? Access it like this:

~~~
>>> print(my_seqs['seq_1'])
GATTACA
~~~

## Still feeling pretty WTF?

That's okay. Let's recap what we just did. We created an empty dictionary and added two key/value pairs to it. The keys and values were all strings in this case, though it's perfectly normal to store other types of data in a dictionary.

Next we printed the entire dictionary, and then we printed just one *value* from the dictionary. Adding items and accessing items both use the same syntax: `dict_name[key]`, which I like to refer to as "square brackets with a key inside, crammed up against the name of the dictionary" notation.

So, was a dictionary the right way to store this data? We could have just stored the whole thing in a string, or put the sequences in a list instead. What's the point of a dictionary?

## Quick lookups

Dictionaries excel at accessing data *one element at a time*. If you added thousands of sequences to your dictionary and then picked a random header to look up, you'd get the corresponding sequence right away[**](#2). 

You can't do this with a string -- you would have to check the entire string for a segment that matches your header, then move forward to find the sequence, and somehow figure out where it ends and the next header begins. Ugh. 

You can't do this with a list, either. Instead, you would have to iterate through the list item by item, checking each header to see if it matches what you're looking for. If your sequence is at the end of the list, too bad! You'll just have to wait until you get there.

## When not to use a dictionary

If dictionaries are great for looking up values, they're pretty lousy for iterating over data. That's not to say you can't do so -- try this simple `for` loop to print your sequences:

~~~
>>> for k in my_seqs.keys():
...     print(my_seqs[k])
...
GATTACA
ACTACTACT
~~~

Calling the `keys()` method on a dictionary will return a list of keys. You're free to loop over these keys and access their corresponding values any time you like. So why would you ever use a plain old list?

There are a couple of reasons. First, there's no point in creating a dictionary if all you need to do is turn it into a list. More importantly, though, dictionaries are *not sorted*. We lucked out getting our seqs back in the order we entered them -- unlike lists, dictionaries offer us no guarantee of that behavior. Want to keep your data in order? Use a list.

## What you need to remember

- Python dictionaries store keys and values
- They are great for when you have to look up single items
- They *do not stay sorted*
- You can create them with curly braces
- You can access them with square brackets


<hr />

<a name="1">*</a><em>Why use </em>`print()`<em>? Doesn't the Python interpreter automatically print the value of a variable when you type its name and press enter?</em> - It does! This tutorial includes the `print()` function, and the extra layer of parentheses that accompany it, in order to encourage careful typing and to provide code samples that will transfer over to a scripting environment.

<a name="2">**</a>Technically speaking, in [constant time](https://wiki.python.org/moin/TimeComplexity).

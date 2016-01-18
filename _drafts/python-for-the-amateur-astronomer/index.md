---
layout: post
title:  "Python for the (amateur) astronomer"
date:   2015-12-16 15:12:07
excerpt: "What are you waiting for? The universe isn't just going to observe itself."
---

Add astronomy to the list of industries and disciplines that have succumbed to the allure of Python. What this means, besides less crufty code for astronomers to maintain, is a wealth of open source, community-managed tools for doing astronomical work -- even if you don't work for NASA. What follows will help you get started doing amateur astronomy with Python.

## A night and day in the life of an astronomer

We should start with a clearer picture of what it is that astronomers actually do. Hint: very little of their time is spent peering into telescopes and naming comets. Today, astronomers harness powerful imaging equipment and data analysis pipelines to learn about the universe.

Observational astronomers run the telescopes. There's a great deal of code involved in the controlling the actual moving parts of a telescope, as well as any immediate image processing pipelines. There's also the job of managing all the image data. Finally, telescopes are expensive to build and maintain, and as such are typically joint ventures who offer their services to scientists worldwide. So some facilities produce custom reservation and scheduling software -- it's like being a sysadmin for a telescope. 

The theoretical work of astronomy involves making sense of huge amounts of image data. Images are filtered and TODO to compensate for known distorting forces. Spectra are analyzed and compared to known TODO. Models are built to explain observed phenomena, then tested and either improved or discarded. 

## Python in astronommy

Astronomers have been solving these problems with code long before Python came on the scene. Historically, the most common language for astronomy has been [IDL](http://www.exelisvis.com/ProductsServices/IDL.aspx) -- a powerful vector programming language first released in 1977. It's got a large scientific library available and it's been the standard for a long enough time at enough research facilities that it's pretty well entrenched.

TODO bubble sort in IDL https://github.com/wlandsman/IDLAstro/blob/master/pro/bsort.pro

However, it's a proprietary language, and while it's efficient at data analysis (e.g. image processing) it's not very well suited for general programming tasks. Compared to Python, which is open source, great for general programming, and supports vector programming with the `numpy` package, IDL is less and less tempting to each new generation of astronomers. (A more thorough comparison of the two languages can be found [here](http://www.astrobetter.com/wiki/tiki-index.php?page=idl_vs_python)).

These bold astronomers who have dared to dream of a free, community-supported astronomical computing environment have made it happen in the form of several astronomy-related Python packages, foremost among which is Astropy.

## Getting started with Astropy

Enough talk, let's install the necessary packages, download some astronomical data, and make a pretty picture.

- Setup and install
- This is attrib only: http://astropy4mpik.readthedocs.org/en/latest/fits.html (more short and sweet)
- This is astropy, so BSD? http://www.astropy.org/astropy-tutorials/FITS-images.html (does more stuff, should prolly use this)
- download a nebula and make a pretty picture

If you're not intimidated by math, and the thought of "calculating the mass of a galaxy from its velocity dispersion" makes you tingle, not shudder, you can go much further with Astropy. Take a look at this [tutorial](http://www.astropy.org/astropy-tutorials/Quantities.html) on using the `Quantities` module.

## Trying out Vispy

Another package with applications to astronomy is Vispy. It's a library for scientific visualization, and ships with a pretty nice spiral galaxy demo. Let's take a quick look.

TODO install

- run spiral galaxy simulation and modify it. BSD license: https://github.com/vispy/vispy/blob/master/examples/demo/gloo/galaxy.py
- modify some stuffs
- wanna X? check out Y.

## What to do next

- Where to get astro data and what it looks like when you get it (FITS format)
  - http://fits.gsfc.nasa.gov/fits_samples.html has a list
- Crowdsourced citizen science astro project (I know the guy, but I forgot the name)
- other projects TODO

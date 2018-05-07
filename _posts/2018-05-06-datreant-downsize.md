---
layout: post
comments: true
title: datreant downsizing
---

The first commit of what became `datreant` occurred over four years ago, and in the course of its development it's seen many iterations on what it is and how it works.
The library didn't even start life as `datreant`: MDSynthesis was born first, with `datreant` becoming a more general library for handling datasets dispersed across a filesystem.

As is often the case with building software, you only really understand what works well and what doesn't by trying something first.
With so much history, `datreant` is finally arriving at a place of stability.
This post is meant to summarize what's coming, and why.

## What will `datreant` look like now?

The biggest change came in [Issue #145](https://github.com/datreant/datreant.core/pull/145).
A directory is now marked as a Treant if it contains a `.datreant` directory.
There are no UUIDs, which could be trouble when copying Treants around.
Tags and Categories are stored individually in their own files in this directory, improving performance when either becomes large.
This change also makes the `discover` machinery more easily able to find Treants,
improving its performance greatly after this was identified as a bottleneck for larger Treant collections.

`datreant` is also no longer a namespace package, and "limbs" have been elminated as a concept.
The original idea we had when we began was that custom limbs, such as that provided by `datreant.data`, could be written and attached to Treants for new functionality.
These could be provided by other packages within the `datreant` namespace, but developed and packaged separately so dependencies of core wouldn't become bloated.
This functionality, however, was difficult to maintain, and writing new limbs wasn't actually easy to do.
What's more, building a CLI interface for Treants was confounded by this complexity.

## Apologies in advance

Open-source software is hard to produce, and it can be even harder to maintain.
In an ideal world, we could roll out gradual changes to `datreant` in a controlled way, according to a clear project plan.
None of our changes would be a huge disruption to users, and we'd do everything technically possible to ease the transition.
But this project is small, with ~3 developers spending a few extra minutes on it every month.
We don't have the bandwidth to do everything the way we want to.

With that, we're releasing `datreant` 0.8.0 in the next few days, with a package on PyPI shortly after.
Please uninstall all `datreant.*` packages from your environment before installing this, as the reversion from a namespace package will lead to unexpected behavior otherwise.

If you are running existing projects using `datreant` and don't want to be affected by these changes
we recommend that you pin your dependency to version 0.7.1.

## Enjoy

We've put literally a couple years' worth of thought into these changes, and we hope they can make `datreant` a better and more sustainable package (and project) into the future.
We value all our users, so please let us know of things that don't work well, and we'll get to fixing them.


-- @dotsdl

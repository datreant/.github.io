---
layout: default
title: datreant
---
#[**datreant**]({{site.baseurl}})
is a project that seeks to make organic exploration and storage of
complex scientific data easier to do. It is also a Python library built around
**Treants**: Python objects that also have a persistent representation in the
filesystem as directory trees, the fundamental data structure of scientific
research.


## The problem

In many fields of science, especially those analyzing experimental or
simulation data, there is often an existing ecosystem of specialized tools and 
file formats which new tools must work around, for better or worse.
Furthermore, centralized database solutions may be suboptimal for data
storage for a number of reasons, including insufficient hardware
infrastructure, variety and heterogeneaity of raw data, the need for data
portability, etc. This is particularly the case for fields centered around
simulation: simulation systems can vary widely in size, composition, rules,
paramaters, and starting conditions. And with increases in computational power,
it is often necessary to store intermediate results obtained from large amounts
of simulation data so it can be accessed and explored interactively.

These problems make data management difficult, and serve as a barrier to
answering scientific questions. To make things easier, **datreant** seeks to
address the tedious and time-consuming logistics of intermediate data storage
and retrieval. It solves a boring problem, so we can focus on interesting ones.


## Availability

The core **datreant** package source is available under the BSD 3-clause license from
[github.com/datreant](https://github.com/datreant). A release is forthcoming. The core
package is provides fairly vanilla components, including the basic **Treant**
object, which are meant to be adapted to more specialized, domain-specific roles
elsewhere. 

As an example, [**MDSynthesis**](https://github.com/datreant/MDSynthesis)
provides **Treants** with functionality specific for working with molecular
dynamics simulations. Addressing the problems of this domain is the original
motivation for **datreant** development, though we welcome others!


## Participating

Feel free to ask questions on the
[datreant](http://groups.google.com/group/datreant) mailing list and join the
discussion.

Please report bugs or enhancement requests for the main package through the
[issue tracker](https://github.com/datreant/datreant/issues). It is not
an overstatement to say that issues drive a lot of development and 
even the direction of the project!

**datreant** is *open source* and welcomes *your* contributions! [Fork the repository
on GitHub](https://github.com/datreant/datreant#fork-destination-box) and
submit a pull request if you have additions you'd like to contribute back.

<a href="https://github.com/datreant"><img style="position: absolute; top: 0; right: 0; border: 0;" src="https://camo.githubusercontent.com/a6677b08c955af8400f44c6298f40e7d19cc5b2d/68747470733a2f2f73332e616d617a6f6e6177732e636f6d2f6769746875622f726962626f6e732f666f726b6d655f72696768745f677261795f3664366436642e706e67" alt="Fork me on GitHub" data-canonical-src="https://s3.amazonaws.com/github/ribbons/forkme_right_gray_6d6d6d.png"></a>

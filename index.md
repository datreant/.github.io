---
layout: default
title: datreant
---
# [**datreant**]({{site.baseurl}})

is a project that seeks to make organic exploration and storage of
complex scientific data easier to do. It is a Python library built around
**Treants**: specially marked directories with distinguishing characteristics
that can be discovered, queried, and filtered. Treants map the filesystem as
it is into a Pythonic interface, making heterogeneous data easier to leverage
while enhancing scientific reproducibility.

See our recent publication in the [SciPy 2016
proceedings](http://conference.scipy.org/proceedings/scipy2016),
and consider citing **datreant**:

* D. L. Dotson, S. L. Seyler, M. Linke, R. J. Gowers, O. Beckstein. [datreant: persistent, Pythonic trees for heterogeneous data](http://conference.scipy.org/proceedings/scipy2016/david_dotson.html). In S. Benthall and S. Rostrup, editors, *Proceedings of the 15th Python in Science Conference*, pages 51-56, Austin, TX, 2016. SciPy.

Also have a look at the brief, 20-minute overview of **datreant** given by
[David Dotson](https://github.com/dotsdl) at [SciPy 2016](http://scipy2016.scipy.org/):

<iframe width="700" height="395" src="http://www.youtube.com/embed/enLHDZoch0U" frameborder="0" allowfullscreen></iframe>

## Why Treants?

In many fields of science, especially those analyzing experimental or
simulation data, there is an existing ecosystem of specialized tools and file
formats which new tools must work around. Often this makes the filesystem serve
as a *de facto* database, with directory trees the zeroth-order data structure
for scientific data. But it can be tedious and error prone to work with these
directory trees to retrieve and store heterogeneous datasets, especially over
projects spanning years with no strict organizational scheme.

Treants make it easy to quickly gather datasets stored within many files in any
format (CSV, HDF5, NetCDF, Feather, etc.) scattered throughout a filesystem,
operate on these data, and store results again as necessary within the Treants'
directory trees. **datreant** also provides Tree and Leaf classes for granular
manipulation of individual directories and files, respectively, as well as
Bundles and Views for working with aggregations of many Treants, Trees, and
Leaves. Bundles in particular can filter Treants based on tags, and perform
group-by operations on their categories. In this way, disparate datasets can be
powerfully manipulated as meta-datasets of Treants. And because Treants are
filesystem objects, they can be used alongside other tools, such as
[dask.distributed](http://distributed.readthedocs.org/), to distill knowledge
from data more effectively.


## Getting datreant

**datreant** is a namespace package, with the core components available in the
dependency-light [datreant.core](http://datreant.readthedocs.org/)
module. All core datreant objects are extendable; an example of this is
[datreant.data](http://datreantdata.readthedocs.org/), which provides a
convenience interface for storing and retrieving `numpy` and `pandas` data
structures in HDF5 using h5py and PyTables internally.

All current datreant subpackages are freely available under a BSD 3-clause
license. See the [installation
instructions](http://datreant.readthedocs.org/en/latest/install.html) to get
set up.


## Domain specificity

**datreant** is also designed with specialized applications for data management
in mind. For working with molecular dynamics (MD) simulation data,
[**MDSynthesis**](http://mdsynthesis.readthedocs.org/)—built on top of
datreant—streamlines workflow through **Sim** objects. **Sims** are special
**Treants** that use [MDAnalysis](http://www.mdanalysis.org/) to dissect MD
trajectories, providing mechanisms for storing system definitions and custom
atom selections. This makes it possible to write maintainable analysis code
that works across many simulation variants. Just as importantly, Sims allow
rapid interactive work drawing from hundreds of simulations at once, making
scientific questions easier to answer with less time and effort.

Interested in building your own domain-specific package on top of datreant?
Let us know on the [mailing list](http://groups.google.com/group/datreant)
so we can help you get rolling!


## Participating

**datreant** is an *open source* project and welcomes your contributions! All
subpackages are openly developed on [GitHub](https://github.com/datreant),
with issues and pull requests always welcome. Check out the [contributor's
guide](http://datreant.readthedocs.org/en/latest/contributing.html) for help
with getting started.

Feel free to ask questions on the
[mailing list](http://groups.google.com/group/datreant) and join the
discussion. This is a great place to get help, propose new ideas for datreant
subpackages, and otherwise get involved with and help steer the project.

<a href="https://github.com/datreant"><img style="position: absolute; top: 0; right: 0; border: 0;" src="https://camo.githubusercontent.com/a6677b08c955af8400f44c6298f40e7d19cc5b2d/68747470733a2f2f73332e616d617a6f6e6177732e636f6d2f6769746875622f726962626f6e732f666f726b6d655f72696768745f677261795f3664366436642e706e67" alt="Fork me on GitHub" data-canonical-src="https://s3.amazonaws.com/github/ribbons/forkme_right_gray_6d6d6d.png"></a>

# README #

This repository links to the [Tilia Manual](http://tilia-manual.readthedocs.org) which support the [Tilia software](http://www.tiliait.com/).

Author:
=======
Simon Goring
Neotoma Development Team

This work is funded through support to the Neotoma Project through NSF Geosciences (award number pending).

We welcome contributions from any individual, whether code, documentation, or issue tracking. All participants are expected to follow the [code of conduct](http://github.com/SimonGoring/tilia-manual/code_of_conduct.md) for this project.

License:
========
The original documentation herein is licensed under an MIT license.  This Documentation makes use of [Sphinx](http://www.sphinx-doc.org/en/stable/) and ReStructuredText.  Sphinx is licensed under a BSD license.

Development
==========
The manual is scripted using plain-text files with [ReStructuredText](http://docutils.sourceforge.net/docs/user/rst/quickstart.html) markdown all saved in the `docs` folder (with an `rst` extension).  [readthedocs](http://readthedocs.org) uses a workflow where documents generated in `rst` files are then compiled to `HTML` using a Python parser called Sphinx to generate the documentation.  Once the file is compiled it is then pushed up to the GitHub repository (you're here now) and is then cloned & re-compiled by readthedocs, where it becomes available at [](http://tilia-manual.readthedocs.org)

Currently the files within the manual are structured (somewhat) hierarchically:

* `index.rst` : The header for the documentation.  Compiles [here](http://tilia-manual.readthedocs.org/en/latest/index.html).  Contains the Acknowledgements and the Table of Contents.  Acts as a simple homepage for the Manual.
* `get_tilia.rst` : Downloading & Installation instructions for Tilia. Compiles [here](http://tilia-manual.readthedocs.org/en/latest/get_tilia.html)
* `creating` : How to create a new Tilia file. Compiles [here](http://tilia-manual.readthedocs.org/en/latest/creating.html)
* `overview.rst` : Presumes that a file has been generated. An overview of an empty Tilia file.  Compiles [here](http://tilia-manual.readthedocs.org/en/latest/overview.html)
* `edit_data.rst` : How to go about editing a Tilia file.  Both practical and best-practices.  Compiles [here](http://tilia-manual.readthedocs.org/en/latest/edit_data.html)
* `tools.rst` : Still a stub.  This is intended to present the various features of Tilia that aren't part of the core editing process. Compiles [here](http://tilia-manual.readthedocs.org/en/latest/tools.html)
* `steward.rst` : Proposed but not developed.

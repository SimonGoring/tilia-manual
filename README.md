# Online Tilia User Manual

[![lifecycle](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://www.tidyverse.org/lifecycle/#experimental)
[![NSF-1948926](https://img.shields.io/badge/NSF-1948926-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1948926)

This repository is the source text for the [Tilia Manual](http://tilia-manual.readthedocs.org) which support the [Tilia software](http://www.tiliait.com/).

## Authors

* Simon Goring
* Jessica Blois
* Neotoma Development Team

This work is funded through support to the Neotoma Project through NSF Geosciences (award number pending).

We welcome contributions from any individual, whether code, documentation, or issue tracking. All participants are expected to follow the [code of conduct](http://github.com/SimonGoring/tilia-manual/code_of_conduct.md) for this project.

## License

The original documentation herein is licensed under an MIT license.  This Documentation makes use of [Sphinx](http://www.sphinx-doc.org/en/stable/) and ReStructuredText.  Sphinx is licensed under a BSD license.

## Development

The manual is scripted using plain-text files with [ReStructuredText](http://docutils.sourceforge.net/docs/user/rst/quickstart.html) markdown all saved in the `docs` folder (with an `rst` extension).  [readthedocs](http://readthedocs.org) uses a workflow where documents generated in `rst` files are then compiled to `HTML` using a Python parser called Sphinx to generate the documentation.  Once the file is compiled it is then pushed up to the GitHub repository (you're here now) and is then cloned & re-compiled by readthedocs, where it becomes available at [](http://tilia-manual.readthedocs.org).

Currently the files within the manual are structured (somewhat) hierarchically:

* `index.rst` : The header for the documentation.  Compiles [here](http://tilia-manual.readthedocs.org/en/latest/index.html).  Contains the Acknowledgements and the Table of Contents.  Acts as a simple homepage for the Manual.
* `get_tilia.rst` : Downloading & Installation instructions for Tilia. Compiles [here](http://tilia-manual.readthedocs.org/en/latest/get_tilia.html)
* `creating` : How to create a new Tilia file. Compiles [here](http://tilia-manual.readthedocs.org/en/latest/creating.html)
* `overview.rst` : Presumes that a file has been generated. An overview of an empty Tilia file.  Compiles [here](http://tilia-manual.readthedocs.org/en/latest/overview.html)
* `edit_data.rst` : How to go about editing a Tilia file.  Both practical and best-practices.  Compiles [here](http://tilia-manual.readthedocs.org/en/latest/edit_data.html)
* `tools.rst` : Still a stub.  This is intended to present the various features of Tilia that aren't part of the core editing process. Compiles [here](http://tilia-manual.readthedocs.org/en/latest/tools.html)
* `steward.rst` : Proposed but not developed.

### Remote Builds

The [`readthedocs`](http://readthedocs.org) website automatically tracks this GitHub repository so that each new `push` to the main branch of this repository triggers the website to rebuild the manual.  Thus, new updates can be immediately seen on the website once either (1) a change is pushed directly to the main branch, or (2) a branch is merged into the main branch through a pull request.

Users who wish to see changes locally _before_ pushing to the repository can build and serve the documentation on their own computers following the directions below:

### Local Builds

To build locally you must have Sphinx installed.  Sphinx is a Python based application, and [instructions for installing sphinx are available here](https://www.sphinx-doc.org/en/master/usage/installation.html).

Once you have ensured that Sphinx is installed you can proceed to the next step.

The folder `docs` contains two `Makefile` type objects.  Once, called `Makefile` and the other called `make.bat`.  The `Makefile` is for Linux-based OSs, including MacOS.  A `Makefile` can be executed using the command `make` followed by a target.  Executing `make` in the `docs` directory will bring up a set of options available as targets.  These include `html`, `epub`, and `latexpdf`.  To see how the documentation will look (approximately) on `readthedocs`, you can execute:

```bash
make html
```

You should see output similar to:

```bash
$ make html
sphinx-build -b html -d _build/doctrees   . _build/html
Running Sphinx v3.2.1
WARNING: html_static_path entry '_static' does not exist
loading pickled environment... done
building [mo]: targets for 0 po files that are out of date
building [html]: targets for 0 source files that are out of date
updating environment: 0 added, 0 changed, 0 removed
looking for now-outdated files... none found
no targets are out of date.
build succeeded, 1 warning.

The HTML pages are in _build/html.

Build finished. The HTML pages are in _build/html.
```

At this point you can open the `~/tilia-manual/docs/_build/html/index.html` file in your browser to see the current representation of the document.  You can navigate through the document, and re-run `make html` any time you make changes to see the current version.

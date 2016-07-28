*****************************
Homestead-Guide
*****************************
|Slack|

.. |Slack| :target: http://slack.expanse.tech

The Expanse Homestead Guide is the reference documentation accompanying the Homestead release of the Expanse project.

`Hosted on ReadTheDocs`_

HOW YOU CAN HELP
================================================================================
**Homestead Documentation Initiative**

It doesn't matter if you are a beginner or an expert, there are many ways to help.

Write Content to the Guide
--------------------------------------------------------------------------------
Write your own content for the guide based on experience.

Make sure the documentation you are porting over is still accurate and follows our guidelines for the Homestead docs (https://expanse-homestead.readthedocs.org/en/latest/about.html).

GETTING STARTED
======================

This project uses Sphinx (http://www.sphinx-doc.org/en/stable/index.html) to build html that is published to Read the Docs. To run this documentation on your computer, you should do the following:

Prerequisites
--------------------------------------------------------------------------------
* Python 2.6 or later
* git

Install Sphinx, etc
--------------------------------------------------------------------------------
For OSX/Linux users (based on instructions here: https://read-the-docs.readthedocs.org/en/latest/getting_started.html)

* From command line: ``sudo pip install sphinx``

For Windows users:

* http://www.sphinx-doc.org/en/stable/install.html#windows-install-python-and-sphinx

Get source code
--------------------------------------------------------------------------------
* git clone: https://github.com/expanse-org/homestead-guide.git

Build and view html
--------------------------------------------------------------------------------
* In a terminal window, go to your homestead-guide directory.
* ``make html``
* ``cd build/html``
* ``open index.html`` (open in web browser)
* Tip: each time you run ``make html``, just reload your browser to view changes


RESOURCES
================================================================================

**Homestead**

* Homestead Guide online: https://expanse-homestead.readthedocs.org/en/latest/index.html

**Read the Docs and Sphinx**

- Read the Docs: https://read-the-docs.readthedocs.org/en/latest/getting_started.html
- Sphinx docs: http://www.sphinx-doc.org/en/stable/contents.html
- reStructuredText Primer: http://www.sphinx-doc.org/en/stable/rest.html
- RST cheat sheet: https://github.com/ralsina/rst-cheatsheet/blob/master/rst-cheatsheet.rst

Directory structure
=========================

.. code-block::

    homestead-guide
      build    - workdir, not commited to repo
      source   - actual content in rst
        conf.py - sphinx configuration
      old-docs-for-reference (Frontier era stuff)
        wiki    - the legacy wiki
        gitbook - the legacy gitbook resources (converted to rst)
      make.bat - windows command to build docs
      Makefile - platforms with make to build docs


.. _Hosted on ReadTheDocs: https://expanse-homestead.readthedocs.org/en/latest/

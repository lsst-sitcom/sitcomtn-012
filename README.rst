.. image:: https://img.shields.io/badge/sitcomtn--012-lsst.io-brightgreen.svg
   :target: https://sitcomtn-012.lsst.io
.. image:: https://github.com/lsst-sitcom/sitcomtn-012/workflows/CI/badge.svg
   :target: https://github.com/lsst-sitcom/sitcomtn-012/actions/

##########################################
Rubin Construction Documentation Inventory
##########################################

SITCOMTN-012
============

This technical note primarily brings together the sources of critical and historical documentation developed across the Rubin Observatory Construction project, with some sources developed by Rubin Observatory Pre-operations and Operations Teams are also included. This inventory is meant as a guide for the Rubin Operations project to determine how and what documentation is transferred as a deliverable from the Construction project. This report is a product of the Documentation Working Group. It responds to charge item 2 in the Charge to the Documentation Working Group, LSE-489. The proposed future state for Rubin Observatory Operations documentation will be reported in another technical report, SITCOMTN-014.

Links
=====

- Live drafts: https://sitcomtn-012.lsst.io
- GitHub: https://github.com/lsst-sitcom/sitcomtn-012

Build
=====

This repository includes lsst-texmf_ as a Git submodule.
Clone this repository::

    git clone --recurse-submodules https://github.com/lsst-sitcom/sitcomtn-012

Compile the PDF::

    make

Clean built files::

    make clean

Updating acronyms
-----------------

A table of the technote's acronyms and their definitions are maintained in the ``acronyms.tex`` file, which is committed as part of this repository.
To update the acronyms table in ``acronyms.tex``::

    make acronyms.tex

*Note: this command requires that this repository was cloned as a submodule.*

The acronyms discovery code scans the LaTeX source for probable acronyms.
You can ensure that certain strings aren't treated as acronyms by adding them to the `skipacronyms.txt <./skipacronyms.txt>`_ file.

The lsst-texmf_ repository centrally maintains definitions for LSST acronyms.
You can also add new acronym definitions, or override the definitions of acronyms, by editing the `myacronyms.txt <./myacronyms.txt>`_ file.

Updating lsst-texmf
-------------------

`lsst-texmf`_ includes BibTeX files, the ``lsstdoc`` class file, and acronym definitions, among other essential tooling for LSST's LaTeX documentation projects.
To update to a newer version of `lsst-texmf`_, you can update the submodule in this repository::

   git submodule update --init --recursive

Commit, then push, the updated submodule.

.. _lsst-texmf: https://github.com/lsst/lsst-texmf

cyko
====

|PyPi Cheese Shop| |Build Status| |Code Quality| |Test Coverage| |License| |DOI|

Konno Omachi filter implemented in Cython.

This code implements Konno-Ohmachi spectral smoothing as defined in::

    Konno, K. and Ohmachi, T., 1998. Ground-motion characteristics estimated
    from spectral ratio between horizontal and vertical components of
    microtremor. Bulletin of the Seismological Society of America, 88(1),
    pp.228-241.

This code was originally written for smoothing sub-module in gmprocess_
by Bruce Worden. Dave Boore has provided notes_
on this topic, which also may be of interest. Notes regarding the
characteristics of the Konno-Ohmachi filter and the implementation are
provided in the implementation_ Jupyter Notebook.

.. _gmprocess: https://github.com/usgs/groundmotion-processing/tree/master/gmprocess/smoothing
.. _notes: http://daveboore.com/daves_notes/notes%20on%20smoothing%20over%20logarithmically%20spaced%20freqs.pd
.. _implementation: implemenation.ipynb

Installation
============

``cyko`` is available via ``pip`` and can be installed with:

::

   pip install cyko

Note that ``cython`` and C compiler are required.

Usage
=====

Smooth a signal using a bandwith of 30.

.. code:: python

   import cyko
   signal_smooth = cyko.smooth(freqs, freqs_raw, signal_raw, 30)

Additional examples and comparison with ``obspy`` are provided in example_.

.. _example: example.ipynb

Citation
========

Please cite this software using the following DOI_.

.. _DOI: https://zenodo.org/badge/latestdoi/183696586

.. |PyPi Cheese Shop| image:: https://img.shields.io/pypi/v/cyko.svg
   :target: https://img.shields.io/pypi/v/cyko.svg
.. |Build Status| image:: https://travis-ci.org/arkottke/cyko.svg?branch=master
   :target: https://travis-ci.org/arkottke/cyko
.. |Code Quality| image:: https://api.codacy.com/project/badge/Grade/a644be36913545708df56fb487e0f9cd
   :target: https://www.codacy.com/manual/arkottke/cyko
.. |Test Coverage| image:: https://api.codacy.com/project/badge/Coverage/a644be36913545708df56fb487e0f9cd    
   :target: https://www.codacy.com/manual/arkottke/cyko
.. |License| image:: https://img.shields.io/badge/license-MIT-blue.svg
.. |DOI| image:: https://zenodo.org/badge/183696586.svg
   :target: https://zenodo.org/badge/latestdoi/183696586

.. GeoCode documentation master file, created by
   sphinx-quickstart on Thu Aug  5 10:11:17 2021.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

GeoCode
===================================

Seismological studies involve intensive coding. Over the years, a large amount of codes have been accumulated. However, they are scattered in the code base of each research group. Some of them are private. It is not easy for newcomers to start a serious seismological research unless they joined a research group that has collected a sufficient group of codes over tens of years. 
Although new algorithms are usually presented clearly in the journal papers, but the basic algorithms they are based on are only briefly mentioned. Implementing the new algorithmms, however, needs implement the basic algorithms as well.

This project aims to provide a collection of code snippets of the basic algorithms that are buiding blocks for advanced methods.

We will provide code snippets instead of a program or library because seismological studies usually needs to experiment a group of different methods in different orders.

Examples
==================================

One-bit normalization
---------------------------------

One-bit normalization turns a time series to a series of -1 and 1 (maybe 0 as well?). It is widely used in processing ambient noise data to suppress the large amplitude events while keeping the phase information (add refs? Shapiro?).

The method turns out to be quite easy to implement. If we use a numpy array ``data`` to represent the time series, the one-bit processed time series can be obtained by

.. code-block:: python3

    import numpy as np
    data_onebit = np.sign(data)



.. toctree::
   :maxdepth: 2
   :caption: Contents:


Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

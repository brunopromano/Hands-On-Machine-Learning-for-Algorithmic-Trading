## Alpha Factor Research & Evaluation

This section introduces the algorithmic trading simulator [`zipline`](http://www.zipline.io/index.html) and the [`alphalens`](http://quantopian.github.io/alphalens/) library for the performance analysis of predictive (alpha) factors.

### `zipline` Installation


#### Installing With ``pip``


Assuming you have all required (see note below) non-Python dependencies, you can install Zipline with ``pip`` via:


    $ pip install zipline

**Note:** Installing Zipline via ``pip`` is slightly more involved than the average Python package.  Simply running ``pip install zipline`` will likely fail if you've never installed any scientific Python packages before.

There are two reasons for the additional complexity:

1. Zipline ships several C extensions that require access to the CPython C API.
   In order to build the C extensions, ``pip`` needs access to the CPython
   header files for your Python installation.

2. Zipline depends on [`numpy`](http://www.numpy.org/>), the core library for
   numerical array computing in Python.  Numpy depends on having the [`LAPACK`](http://www.netlib.org/lapack) linear algebra routines available.

Because LAPACK and the CPython headers are binary dependencies, the correct way to install them varies from platform to platform.  On Linux, users generally acquire these dependencies via a package manager like `apt`, `yum`, or `pacman`.  On OSX, `[Homebrew](http://www.brew.sh) is a popular choice
providing similar functionality.

See the full [Zipline Install Documentation](https://github.com/quantopian/zipline#installation) for more information on acquiring binary dependencies for your specific platform.

#### Installing with `conda`

Another way to install Zipline is via the `conda` package manager, which comes as part of [`Anaconda`](http://continuum.io/downloads) or can be installed via `pip install conda`.

Once set up, you can install Zipline from the `Quantopian` channel:

    $ conda install -c Quantopian zipline

Currently supported platforms include:

-  GNU/Linux 64-bit
-  OSX 64-bit
-  Windows 64-bit

.. note::

   Windows 32-bit may work; however, it is not currently included in
   continuous integration tests.


### `alphalens` Installation

Install with pip:

    pip install alphalens

Install with conda:

    conda install -c conda-forge alphalens

Install from the master branch of the Alphalens repository (development code):

    pip install git+https://github.com/quantopian/alphalens

Alphalens depends on:

-  [`matplotlib`]( <https://github.com/matplotlib/matplotlib)
-  [`numpy`](https://github.com/numpy/numpy)
-  [`pandas`](https://github.com/pydata/pandas)
-  [`scipy`](https://github.com/scipy/scipy)
-  [`seaborn`](https://github.com/mwaskom/seaborn)
-  [`statsmodels`](https://github.com/statsmodels/statsmodels)

.. image:: https://img.shields.io/coveralls/github/timcera/tsgettoolbox_twc
    :alt: Test Coverage
    :target: https://coveralls.io/r/timcera/tsgettoolbox_twc?branch=master
    :height: 20

.. image:: https://img.shields.io/pypi/v/tsgettoolbox_twc
    :alt: Latest release
    :target: https://pypi.python.org/pypi/tsgettoolbox_twc/
    :height: 20

.. image:: https://img.shields.io/pypi/l/tsgettoolbox_twc
    :alt: BSD-3 clause license
    :target: https://pypi.python.org/pypi/tsgettoolbox_twc/
    :height: 20

.. image:: https://img.shields.io/pypi/pyversions/tsgettoolbox_twc
    :alt: PyPI - Python Version
    :target: https://pypi.org/project/tsgettoolbox_twc/
    :height: 20

tsgettoolbox_twc - Quick Guide
==============================
The 'tsgettoolbox_twc' is a plugin-in for 'tsgettoolbox' that supplies
a command line interface and Python library to get time-series data from the
Texas Weather Connection (TWC).  The tsgettoolbox_twc will work with
Python 3.10+.

Documentation
-------------
Reference documentation is at `tsgettoolbox_documentation`_.

Installation
------------
At the command line::

    $ pip install tsgettoolbox_twc

    OR

    $ conda install -c conda-forge tsgettoolbox_twc

Usage Summary - Command Line
----------------------------
Just run 'tsgettoolbox --help' to get a list of subcommands.  To get detailed
help for a particular sub-command, for instance 'twc', type 'tsgettoolbox
twc --help'.

+-------------+---------+--------+---------+----------+-----------------------+
| Sub-command | Spatial | Time   | Type    | Time     | Description           |
|             | Extent  | Extent |         | Interval |                       |
+=============+=========+========+=========+==========+=======================+
| twc         | US/OK   | varies | station | D        | Texas Weather         |
|             |         |        |         |          | Connection (TWC) data |
+-------------+---------+--------+---------+----------+-----------------------+

+-------------------+-------------+
| Time Interval     | Description |
| Code              |             |
+===================+=============+
| D                 | Daily       |
+-------------------+-------------+

Usage Summary - Python Library
------------------------------
To use the tsgettoolbox in a project::

    from tsgettoolbox import tsgettoolbox
    df = tsgettoolbox.twc(48501, start_date="2015-11-04", end_date="2015-12-05")
    print(df.head())

Refer to the API Documentation at `tsgettoolbox_api`_.

Usage Summary - Command Line
----------------------------

    tsgettoolbox twc 48501 --start_date 2015-11-04 --end_date 2015-12-05

Refer to the command line documentation at `tsgettoolbox_cli`_.

Development
~~~~~~~~~~~
Development is managed on bitbucket or github.
https://bitbucket.org/timcera/tsgettoolbox_twc/overview.
https://github.com/timcera/tsgettoolbox_twc

.. _tsgettoolbox_documentation: https://timcera.bitbucket.io/linked_pkg_dirs/tsgettoolbox/docs/index.html
.. _tsgettoolbox_api: https://timcera.bitbucket.io/linked_pkg_dirs/tsgettoolbox/docs/function_summary.html
.. _tsgettoolbox_cli: https://timcera.bitbucket.io/linked_pkg_dirs/tsgettoolbox/docs/command_line.html

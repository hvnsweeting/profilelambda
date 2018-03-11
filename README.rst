=============
profilelambda
=============


.. image:: https://img.shields.io/pypi/v/profilelambda.svg
        :target: https://pypi.python.org/pypi/profilelambda

.. image:: https://img.shields.io/travis/hvnsweeting/profilelambda.svg
        :target: https://travis-ci.org/hvnsweeting/profilelambda

.. image:: https://readthedocs.org/projects/profilelambda/badge/?version=latest
        :target: https://profilelambda.readthedocs.io/en/latest/?badge=latest
        :alt: Documentation Status


.. image:: https://pyup.io/repos/github/hvnsweeting/profilelambda/shield.svg
     :target: https://pyup.io/repos/github/hvnsweeting/profilelambda/
     :alt: Updates



Decorators and utils for profiling / debugging functions - especially AWS lambda

Just adding one line for debug called arguments and profiling your function.
Your AWS lambda can be triggered by different source of events, thus, different
arguments.

* Free software: MIT license


Features
--------

- Single code line for profiling decorated function
- Also print out called arguments for debugging

Example
-------

Your broken function::

  def lambda_handler(event, context):
      do_something()

Adding profiler and argument debugging::

  from profilelambda import profile


  @profile
  def lambda_handler(event, context):
      print("Hello this is my lambda")

Output::

  Function 'lambda_handler' got arguments ({}, None) and keyword arguments {}
  Hello this is my lambda

  *** PROFILER RESULTS ***
  lambda_handler (test.py:4)
  function called 1 times

           2 function calls in 0.000 seconds

     Ordered by: cumulative time, internal time, call count

     ncalls  tottime  percall  cumtime  percall filename:lineno(function)
          1    0.000    0.000    0.000    0.000 test.py:4(lambda_handler)
          1    0.000    0.000    0.000    0.000 {method 'disable' of '_lsprof.Profiler' objects}
          0    0.000             0.000          profile:0(profiler)

Credits
-------

This package was created with Cookiecutter_ and the `audreyr/cookiecutter-pypackage`_ project template.

.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`audreyr/cookiecutter-pypackage`: https://github.com/audreyr/cookiecutter-pypackage

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
      do_something()

Credits
-------

This package was created with Cookiecutter_ and the `audreyr/cookiecutter-pypackage`_ project template.

.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`audreyr/cookiecutter-pypackage`: https://github.com/audreyr/cookiecutter-pypackage

|Build status| |Documentation Status|

newslynx-sc-facebook
====================

Installation
------------

Production
~~~~~~~~~~

To install ``newslynx-sc-facebook`` for an active installation of
``newslynx-core``, run the following command:

.. code:: bash

    $ newslynx sc-install https://github.com/newslynx/newslynx-sc-facebook.git

To add ``newslynx-sc-facebook`` all orgnaizations, run:

.. code:: bash

    $ newslynx sc-sync

Development
~~~~~~~~~~~

If you want to modify / add Sous Chefs to ``newslynx-sc-facebook``, do
the following:

**NOTE** Will install a fresh version of ``newslynx`` via ``pip``.

.. code:: bash

    $ git clone https://github.com/newslynx/newslynx-sc-facebook.git
    $ cd newslynx-sc-facebook
    $ pip install --editable .

You should now be able to run ``newslynx-sc-facebook``'s Sous Chefs in
development mode

.. code:: bash

    % newslynx sc-run newslynx_sc_facebook/say_my_name.yaml --myname='Brian Abelson'

Tests
-----

Requires ``nose``

.. code:: bash

    $ make all_tests

Documentation
-------------

Documentation for ``newslynx-sc-facebook`` is hosted on `Read The
Docs <http://newslynx-sc-facebook.readthedocs.org/>`__.

It's generated via the following steps

-  converts this file (``README.md``) into a ReStructured Text file,
   saving it to
   `docs/index.rst <https://github.com/newslynx/newslynx-sc-facebook/blob/master/docs/index.rst>`__
-  runs ``newslynx sc-docs newslynx_sc_facebook -f rst`` to generate
   documentation for all the Sous Chefs in ``newslynx-sc-facebook`` and
   saves the output to
   `docs/sous-chefs.rst <https://github.com/newslynx/newslynx-sc-facebook/blob/master/docs/sous-chefs.rst>`__
-  Builds Sphinx Documentation from these files.

Continuous Integration
----------------------

Builds for ``newslynx-sc-facebook`` can be found on
`Travis <https://travis-ci.org/newslynx/newslynx-sc-facebook>`__

Contributing
------------

See the `contributing
guidelines <https://github.com/newslynx/newslynx-sc-facebook/blob/master/CONTRIBUTING.md>`__.

What's in this module ?
-----------------------

-  `README.md <https://github.com/newslynx/newslynx-sc-facebook/blob/master/README.md>`__

   -  This file

-  `VERSION <https://github.com/newslynx/newslynx-sc-facebook/blob/master/VERSION>`__

   -  ``newslynx-sc-facebook``'s source-of-truth version.

-  `requirements.txt <https://github.com/newslynx/newslynx-sc-facebook/blob/master/requirements.txt>`__

   -  ``newslynx-sc-facebook``'s python dependencies.

-  `MANIFEST.in <https://github.com/newslynx/newslynx-sc-facebook/blob/master/MANIFEST.in>`__

   -  Specifications for which files to include in the PyPI
      distribution.
   -  See the docs on this
      `here <https://docs.python.org/2/distutils/sourcedist.html#specifying-the-files-to-distribute>`__.

-  `setup.py <https://github.com/newslynx/newslynx-sc-facebook/blob/master/setup.py>`__

   -  Specification's for building ``newslynx-sc-facebook``'s PyPI
      distribution.

-  `.travis.yml <https://github.com/newslynx/newslynx-sc-facebook/blob/master/.travis.yml>`__

   -  Configurations for Travis Continuous Integration
   -  You must activate this project on
      `travis-ci.org <https://github.com/newslynx/newslynx-sc-facebook/blob/master/http://travis-ci.org/>`__
      for this to run on subsequent updates.

-  `Makefile <https://github.com/newslynx/newslynx-sc-facebook/blob/master/Makefile>`__

   -  Helpers for managing ``newslynx-sc-facebook``.
   -  Includes:

      -  ``make clean``:

         -  Cleans out cruft from this directory.

      -  ``make install``:

         -  Installs ``newslynx-sc-facebook``. Assumes that you're in a
            virtual environment.

      -  ``make all_tests``:

         -  Runs the tests.

      -  ``make readme``

         -  Converts this file to ``.rst``, including a table of
            contents, and saves it to
            `docs/index.rst <https://github.com/newslynx/newslynx-sc-facebook/blob/master/docs/index.rst>`__

      -  ``make sous_chef_docs``

         -  Programmtically generates `Sous Chef
            documentation <https://github.com/newslynx/newslynx-sc-facebook/blob/master/docs/sous-chefs.rst>`__
            by running
            ``newslynx sc-docs newslynx_sc_facebook/ --format=rst > docs/sous-chefs.rst``.

      -  ``make all_docs``:

         -  Builds the sphinx docs for ``newslynx-sc-facebook`` by
            running the above two commands.

      -  ``make view_docs``

         -  Serves documentation at
            `localhost:8000 <http://localhost:8000>`__

      -  ``make register``:

         -  Registers ``newslynx-sc-facebook`` on
            `PyPI <https://pypi.python.org/pypi>`__.

      -  ``make distribute``:

         -  Publishes a new version of ``newslynx-sc-facebook`` to PyPI.

-  `CONTRIBUTING.md <https://github.com/newslynx/newslynx-sc-facebook/blob/master/CONTRIBUTING.md>`__

-  `newslynx\_sc\_facebook <https://github.com/newslynx/newslynx-sc-facebook/blob/master/newslynx_sc_facebook/>`__

   -  ``newslynx-sc-facebook``'s source code and Sous Chef configuration
      files.

-  `docs <https://github.com/newslynx/newslynx-sc-facebook/blob/master/docs/>`__

   -  Sphnix documentation for ``newslynx-sc-facebook``

-  `tests <https://github.com/newslynx/newslynx-sc-facebook/blob/master/tests/>`__

   -  ``nose`` tests for ``newslynx-sc-facebook``

.. |Build status| image:: https://travis-ci.org/newslynx/newslynx-sc-facebook.svg
   :target: https://travis-ci.org/newslynx/newslynx-sc-facebook
.. |Documentation Status| image:: https://readthedocs.org/projects/newslynx-sc-facebook/badge/?version=latest
   :target: https://readthedocs.org/projects/newslynx-sc-facebook/?badge=latest

Contents
--------
.. toctree::
	:maxdepth: 2

	index
	sous-chefs

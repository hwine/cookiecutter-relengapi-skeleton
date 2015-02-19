=============================
cookiecutter-releng-pylibrary
=============================

`Cookiecutter <https://github.com/audreyr/cookiecutter>`_ template for a
`RelEngApi skeleton
<https://github.com/mozilla/build-relengapi-skeleton>`_ setup.

Features
--------

* Mozilla Public License
* Travis-CI_ and Coveralls_ for continuous testing and coverage tracking.
* Documentation with Sphinx_.

Requirements
------------

Projects using this template have these minimal dependencies:

* Setuptools_ - for building the package, wheels etc. Now-days Setuptools is widely available, it shouldn't pose a
  problem :)
* All the packages needed for relengapi development

Usage
-----

Generate your project::

    cookiecutter https://github.com/hwine/cookiecutter-relengapi-skeleton

..

    .. list-table:: The variables
        :stub-columns: 1

        * - project_name
          - Verbose project name, used in headings (docs, readme, etc)
        * - repo_name
          - Repository name on github
        * - github_username
          - username where repository will initially live
        * - package_name
          - Python package name (whatever you would import)
        * - distribution_name
          - PyPI distribution name (what you would ``pip install``)

After this you can create the initial repository (make sure you `create <https://github.com/new>`_ an *empty* Github
project)::

    git init .
    git add .
    git commit -m "Initial skel."
    git remote add origin git@github.com:${github_user_name}/${new_repo_name}
    git push -u origin master

Then:

* `Enable the repository in your Travis CI account <https://travis-ci.org/profile>`_.
* `Enable the repository in your Coveralls account <https://coveralls.io/repos/new>`_.
* Release your package. This template comes with a tox environment (``check``) that will:

  * Check if your ``README.rst`` is valid.
  * Check if the ``MANIFEST.in`` has any issues.
  * Run ``flake8`` (a combo of PEP8, pyflakes and McCabe checks)

Not Exactly What You Want?
--------------------------

If you have criticism or suggestions please open up an Issue or Pull Request.

.. _Travis-CI: http://travis-ci.org/
.. _Tox: http://testrun.org/tox/
.. _Sphinx: http://sphinx-doc.org/
.. _Coveralls: https://coveralls.io/
.. _ReadTheDocs: https://readthedocs.org/
.. _Setuptools: https://pypi.python.org/pypi/setuptools
.. _Pytest: http://pytest.org/

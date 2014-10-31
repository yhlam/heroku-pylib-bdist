Python Library Binary Distributions for Heroku
==============================================

Pre-build packages of python library for Heroku server. All libraries are built
on Ubuntu 10.04 64bit VM, which matches the Heroku's server environment.

List of Library
---------------

* numpy 1.9.0
* scipy 0.14.0
* scikit-learn 0.15.2

List of Binary Dependency
-------------------------

* gfortran
* libatlas-base-dev
* libblas-dev
* liblapack-dev

Usage
-----

* Extract the binary dependencies into /app/.heroku/python/.
* Install the python libraries with ``pip install --no-index --find-links=path_to_heroku_pylib_bdist``.
* Example install script for heroku compile hook is in example/install_pylib_bdist.

Development
-----------

The binaries are built with vagrant and ansible. To compile the binaries by
yourself, you will need to install virtualbox, vagrant and ansible.

Run::
    vagrant up --provision

Or::
    vagrant provision

The binaries will be compiled into the build directory.

License
-------

The ansible playbook for this project is released under the MIT license.

How to build the plugin from source
===================================

To build the plugin, you first need to install fuel-plugin-builder_ 4.1.0

.. code-block:: bash

  $ pip install fuel-plugin-builder==4.1.0

Build the plugin:

.. code-block:: bash

  $ git clone https://git.openstack.org/openstack/fuel-plugin-nsx-t

  $ cd fuel-plugin-nsx-t/

The librarian-puppet_ ruby package is required to be installed. It is used to fetch
upstream fuel-library_ puppet modules that the plugin uses. It can be installed via
the *gem* package manager:

.. code-block:: bash

  $ gem install librarian-puppet

or if you are using ubuntu linux, you can install it from the repository:

.. code-block:: bash

  $ apt-get install librarian-puppet

and build the plugin:

.. code-block:: bash

  $ fpb --build .

fuel-plugin-builder will produce an .rpm package of the plugin which you need to
upload to the Fuel master node:

.. code-block:: bash

  $ ls nsx*.rpm

  nsx-t-1.0-1.0.0-1.noarch.rpm

.. _fuel-plugin-builder: https://pypi.python.org/pypi/fuel-plugin-builder/4.1.0
.. _librarian-puppet: http://librarian-puppet.com
.. _fuel-library: https://github.com/openstack/fuel-library

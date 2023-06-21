=========
ElectrumX
=========

This project is a detached `fork' of `spesmilo/electrumx <https://github.com/spesmilo/electrumx>`_.

ElectrumX allows users to run their own Electrum server. It connects to your
full node and indexes the blockchain, allowing efficient querying of history of
arbitrary addresses. The server can be exposed publicly, and joined to the public network
of servers via peer discovery. As of May 2020, a significant chunk of the public
Electrum server network runs ElectrumX.

The current version is |wip|.

Source Code
===========

The project is hosted on `GitHub
<https://github.com/dev-warrior777/electrumx-dash/>`_.

Please submit an issue on the `bug tracker
<https://github.com/dev-warrior777/electrumx-dash/issues>`_ if you have found a
bug or have a suggestion to improve the server. Not for Windows.

Authors and License
===================

Neil Booth wrote the vast majority of the code; see :ref:`Authors`.
Python version at least 3.10 is required.

The code is released under the `MIT Licence
<https://github.com/dev-warrior777/electrumx-dash/LICENCE>`_.

Getting Started
===============

See :ref:`HOWTO`.

There is also an `installer`_ available that simplifies the
installation on various Linux-based distributions, and a `Dockerfile`_
available .

.. _installer: https://github.com/bauerj/electrumx-installer
.. _Dockerfile: https://github.com/lukechilds/docker-electrumx

Documentation
=============

.. toctree::

   features
   changelog
   HOWTO
   environment
   protocol
   peer_discovery
   rpc-interface
   architecture
   authors

Indices and tables
==================

* :ref:`genindex`
* :ref:`search`

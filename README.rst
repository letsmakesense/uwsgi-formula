======
uwsgi
======

Set up and configure the uwsgi server framework.
This module is based on the excelent work done in the nginx-formula by the
contributors.

.. note::

    See the full `Salt Formulas installation and usage instructions
    <http://docs.saltstack.com/en/latest/topics/development/conventions/formulas.html>`_.

Available states
================

.. contents::
    :local:

``uwsgi``
---------

Metastate to Install uwsgi from the system package manager. Note, the uwsgi version
available varies by platform.

**Note:** uwsgi requires the merge parameter of salt.modules.pillar.get(),
first available in the Helium release.

Example usage::

    include:
      - uwsgi

``uwsgi.install``
-----------------

Installs the uwsgi package

``uwsgi.application_config``
----------------------------

Manages the application files for the uwsgi server

``uwsgi.pip``
-------------

Install uwsgi via pip.

``uwsgi.plugins``
-----------------

Install uwsgi plugins via default package management system.
plugins can be specified via pillar lookup function.

``uwsgi.emperor``
-----------------

Meta state to install and confgure uwsgi emperor via default package management system.

Example usage::

    include:
      - uwsgi.emperor

``uwsgi.emperor.config``
------------------------

Manages the uwsgi emperor config file, all variables can be set by pillar

``uwsgi.emperor.install``
-------------------------

Manages the installation of uwsgi package

``uwsgi.emperor.vassal_config``
-------------------------------

Manages the vassal files for the uwsgi emperor process

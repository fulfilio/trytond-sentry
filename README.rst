Sentry for Tryton
=================

Sentry is a realtime event logging system. This module provides a tryton
daemon script which reports unhandled exceptions to sentry and sends a
friendly message to the client with an identifier of the error code.
The daemon script `trytond_sentry` is a drop in replacement for `trytond`
installed by the trytond official package.

Build Status (Master)
---------------------

.. image:: https://travis-ci.org/fulfilio/trytond-sentry.svg?branch=master
    :target: https://travis-ci.org/fulfilio/trytond-sentry

Build Status (Develop)
----------------------

.. image:: https://travis-ci.org/fulfilio/trytond-sentry.svg?branch=develop
    :target: https://travis-ci.org/fulfilio/trytond-sentry

Screenshots
-----------

.. image:: https://www.github.com/fulfilio/trytond-sentry/raw/master/images/message.png
.. image:: https://www.github.com/fulfilio/trytond-sentry/raw/master/images/grouplist.png
.. image:: https://www.github.com/fulfilio/trytond-sentry/raw/master/images/event.png
.. image:: https://www.github.com/fulfilio/trytond-sentry/raw/master/images/modules.png

Installation
------------

From PyPI::

    pip install trytond_sentry

For older versions::

    pip install 'trytond_sentry>=2.8,<3.0'

From git repository::

    git clone git@github.com:fulfilio/trytond-sentry.git
    cd trytond-sentry
    python setup.py install

Usage
-----

The DSN is an additional argument required for the daemon script to
know which sentry server the errors should be reported to. This can
be specified in two ways:

1. As a command line argument::

    trytond_sentry -s http://<public_key>:<secret_key>@sentry.com/1

2. In the configuration::

    trytond_sentry -c /path/to/config

where the config file has an argument ::

  sentry_dsn = http://<public_key>:<secret_key>@sentry.com/1

Changelog
---------

Read CHANGELOG

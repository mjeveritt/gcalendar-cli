============
gcalendar-cli
============

Command-line Interface for Google Calendar

.. image:: https://badge.fury.io/py/gcalendar-cli.svg
   :target: http://badge.fury.io/py/gcalendar-cli
   :alt: PyPI version

.. image:: https://travis-ci.org/mjeveritt/gcalendar-cli.svg?branch=master
   :target: https://travis-ci.org/mjeveritt/gcalendar-cli
   :alt: Build Status

.. image:: https://coveralls.io/repos/mjeveritt/gcalendar-cli/badge.svg?branch=master&service=github
   :target: https://coveralls.io/github/mjeveritt/gcalendar-cli?branch=master
   :alt: Coverage Status

.. image:: https://img.shields.io/badge/license-Apache%202.0-blue.svg
   :target: http://choosealicense.com/licenses/apache-2.0/
   :alt: License

.. image:: https://badge.waffle.io/mogproject/calendar-cli.svg?label=ready&title=Ready
   :target: https://waffle.io/mogproject/calendar-cli
   :alt: 'Stories in Ready'

------------
Dependencies
------------

* Python: 2.7 / 3.4+
* six
* python-dateutil
* pytz
* tzlocal
* google-api-python-client
* argparse
* `mog-commons <https://github.com/mogproject/mog-commons-python>`_

------------
Installation
------------

* ``pip`` command may need ``sudo``

+-------------------------+------------------------------------------+
| Operation               | Command                                  |
+=========================+==========================================+
| Install                 |``pip install gcalendar-cli``             |
+-------------------------+------------------------------------------+
| Upgrade                 |``pip install --upgrade gcalendar-cli``   |
+-------------------------+------------------------------------------+
| Uninstall               |``pip uninstall gcalendar-cli``           |
+-------------------------+------------------------------------------+
| Check installed version |``gcalendar-cli --version``                |
+-------------------------+------------------------------------------+
| Help                    |``gcalendar-cli -h``                       |
+-------------------------+------------------------------------------+

---------------
Getting Started
---------------

1. Download ``client_secret.json`` from Google Developers Console
   
* Open `Google API Manager <https://console.developers.google.com/apis/credentials>`_
* Select or create a project
* Open API Manager -> Credentials

  * OAuth consent screen: Set a product name and save
  * Credentials: Add credentials -> OAuth 2.0 client ID -> Other: Set a name and create
  * Download a credential file by clicking the ``Download JSON`` button, then rename it ``client_secret.json``

2. Create a credentials file

::

    gcalendar-cli setup client_secret.json

The default path to the credentials file is ``~/.credentials/gcalendar-cli.json``.

3. Print the summary of today's events on the default calendar

::

    gcalendar-cli


* Launch with arguments

::

    gcalendar-cli --date 20151014
    gcalendar-cli --calendar xxxxxx@group.calendar.google.com


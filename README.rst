Prerequisites
=====================

.. code-block:: bash

   easy_install pip
   pip install -r requirements.txt


Build
=====================

English
---------------------

.. code-block:: bash

   make livehtml

Japanese
---------------------

.. code-block:: bash

   make -e SPHINXOPTS="-c ja" SOURCEDIR="ja" livehtml

view built html
---------------------

access to http://localhost:8000

Translate
---------------------

#. create pot files.

   .. code-block:: bash

      make gettext

#. update locales.

   .. code-block:: bash

      make intlupdate

#. edit po files in ``locale/ja/LC_MESSAGES``

#. build locales.

   .. code-block:: bash

      make intlbuild


Directories
=====================

* ``source``

  Contains document sources in English.

* ``locale``

  Contains gettext translation files (``po`` files).

* ``ja`` etc. (Locale name directory)

  Contains document sources in Japanese etc.
  These directories are used to build documents on readthedocs.org in each locales.

  Basically, these directories contain symlinks to ``source`` directory contents (excluding ``locale`` directory), and have locale specific ``conf.py``.
  But if you want to add pages not contained in ``source`` directory, simply add ``rst`` file in this directory. 

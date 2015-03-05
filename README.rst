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

   make -e SPHINXOPTS="-c ja" livehtml

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

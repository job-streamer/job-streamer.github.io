## Install

.. code-block: bash

   pip install -r requirements.txt

## Build

### en

.. code-block: bash

   make html

### ja

.. code-block: bash

   make -e SPHINXOPTS="-c source/locale/ja" html

## Translate

create pot files.

.. code-block: bash

   make clean gettext

update locales.

.. code-block: bash

   sphinx-intl update -p build/locale -l ja

build locales.

.. code-block: bash

   sphinx-intl build

.. job-streamer documentation master file, created by
   sphinx-quickstart on Tue Feb 24 15:01:20 2015.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

.. toctree::
   :hidden:

   setup
   developer-guide

JobStreamer
==============

.. image:: _images/overview.png

JobStreamerは、JavaBatchの分散実行環境です。設定やデプロイなしで実行環境をクラウド上に構築できるため、負荷量に応じて非常に簡単に実行環境を増減させることが出来ます。

JavaBatchでは規格化されていないJobのスケジュール実行も可能です。

------------
Concept
------------

* `Agent`_ はノーデプロイ、ノーコンフィギュレーション。仮想イメージを立ち上げると瞬時にジョブ実行サーバとなります。
* `Management console`_ は `Control bus`_ のフロントエンドで、Control busの提供するAPIから取得した結果を表示する機能だけを持ちます。

------------
Get started
------------

- :doc:`setup`
- Create a job
- Deploy jobs

------------
Components
------------

- `Control bus`_
- `Agent`_
- `Management console`_

.. _Control bus:        https://github.com/job-streamer/job-streamer-control-bus
.. _Agent:              https://github.com/job-streamer/job-streamer-agent
.. _Management console: https://github.com/job-streamer/job-streamer-console



.. toctree::
   :hidden:

   setup
   developer-guide
   create-job
   deploy-jobs

JobStreamer
==============

.. image:: _images/overview.png

------------
コンセプト
------------

JobStreamerは、JavaBatchの分散実行環境です。設定やデプロイなしで実行環境をクラウド上に構築できるため、負荷量に応じて非常に簡単に実行環境を増減させることが出来ます。

JavaBatchでは規格化されていないJobのスケジュール実行も可能です。

* `Agent`_ はノーデプロイ、ノーコンフィギュレーション。仮想イメージを立ち上げると瞬時にジョブ実行サーバとなります。
* `Management console`_ は `Control bus`_ のフロントエンドで、Control busの提供するAPIから取得した結果を表示する機能だけを持ちます。

------------
起動
------------

- :doc:`get-started-developer`
- :doc:`get-started-quickly`

------------
使い方
------------
- :doc:`deploy-batch-components`
- :doc:`create-a-job`
- :doc:`execute-the-job`
- :doc:`schedule-job`
- :doc:`job-config`
- :doc:`notificator-config`

------------
部品
------------

- `Control bus`_
- `Agent`_
- `Management console`_
- `Notificator`_

.. _Control bus:        https://github.com/job-streamer/job-streamer-control-bus
.. _Agent:              https://github.com/job-streamer/job-streamer-agent
.. _Management console: https://github.com/job-streamer/job-streamer-console
.. _Notificator:        https://github.com/job-streamer/job-streamer-notificator

------------
ガイド
------------
- :doc:`developer-guide`

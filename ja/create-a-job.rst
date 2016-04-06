.. highlight:: guess

ジョブの作成
===========

ジョブの作成
--------------

1. トップページ(http://{サーバ機のIPアドレス}:{コンソールの立ち上げポート番号（デフォルトは8080)})にて"new"ボタンを押下

.. image:: _images/new_job_button.png
 :width: 100%
 
2. Scratchの要領で、ドラッグ＆ドロップにてジョブを作成

.. image:: _images/new_job.png
 :width: 100%

BatchletやItemReader/ItemWriter/ItemProcessorはコントロールバスにデプロイされているものだけが使用できます。
新しいバッチ部品を使用したい場合は :doc:`deploy-batch-components` を参照してください。

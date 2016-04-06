.. highlight:: guess

バッチ部品のデプロイ
===========

デプロイ手法
--------------

`maven plugin`_ を用いてバッチ部品をコントロールバス上にデプロイします。
そのため、バッチ部品はmavenプロジェクトで作成することを推奨します。

.. _`maven plugin` https://github.com/job-streamer/job-streamer-maven-plugin

例
--------------

1. Exampleを取得::

   % git clone https://github.com/job-streamer/job-streamer-examples.git

2. デプロイ::

   % cd job-streamer-examples
   % mvn -e clean package job-streamer:deploy
  
  デプロイを行うにはデプロイ資源とcontrol busが同じサーバーに存在する必要があります。
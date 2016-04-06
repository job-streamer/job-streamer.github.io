.. highlight:: guess
ジョブのスケジューリング
===========

スケジュールで自動実行する
--------------
`quartz`_ 形式でスケジュールを登録することで、ジョブを自動実行できます。

.. _quartz: http://quartz-scheduler.org/api/2.2.0/org/quartz/CronExpression.html

.. image:: _images/schedule_quartz.png
 :width: 100%

カレンダーの登録方法
--------------
1.トップページから右側メニューのプルダウン選択によりカレンダーに移動

.. image:: _images/goto-calendar.png
 :width: 100%
 
2.newボタン押下

.. image:: _images/goto-calendar-new.png
 :width: 100%
 
3.カレンダーを作成

.. image:: _images/goto-calendar.png
 :width: 100%
 
カレンダーを設定して休日はジョブの実行を抑止する
--------------
quartz形式とともにカレンダーも設定することでカレンダーに休日として登録されている日はジョブの実行を抑止することができます。

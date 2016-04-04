.. highlight:: guess
通知サーバの設定
==============

ednファイルを用いてルールの設定を行います。
Ex. ::


  { :do-job {:uri "http://localhost:45102/default/job/success-mail/executions?Exchange.CONTENT_TYPE=application/edn"
             :message "{}"}
  }

This means that if ":do-job" key was sent to notificator, POST to "http://localhost:45102/default/job/success-mail/executions?Exchange.CONTENT_TYPE=application/edn".
So that "success-mail" job run.

*It needs that Control bus and Notificator are in same server.

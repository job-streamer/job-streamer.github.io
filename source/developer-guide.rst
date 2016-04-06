
JobStreamer developer guide
========================================

----------------------------------------
Format policy
----------------------------------------

* All of exchange data is done using `EDN Format`_ .（In comparison with the JSON, there is an advantage that it is possible to have a type of `` Date`` and `` UUID``. ）
* Map key in EDN is keyword with entity's name-space. (Easy to understand when see only data.)

----------------------------------------
Interface policy
----------------------------------------

* Both Agent and Control bus use REST API as interface.（Enable tool development Other than Console）
* Must call from Control bus to Agent API.Don't Occur reverse call. 

----------------------------------------
connection policy
----------------------------------------

* In order to Improve responsivility of Agent,WebSocket connect bus from agent  to Control.
* Consideration of failure,WebSocket doesn't exchange data,only notification.
* Monitoring dead or alive and performance of Agent. 
* In order to make Agen no configuration,detect Control bus altomatically.

  #. Agent broadcast its own address just it starts running.
  #. If Control bus caught broadcast from Agent, send connection request to Agent.
  #. Agent that recieve connection request try to WebSocket connect toControl bus.

* When shut down connection from Agent to Control,Agent restart broadcast,so that even if switch Control bus stand-by,repair connection altomatically.

----------------------------------------
Persitence policy
----------------------------------------

* All data flowing at Control bus stores Datomic.
* Accessing to Datomic allow only from Control bus.

----------------------------------------
If you want more safely structure
----------------------------------------

* Because `WebSocketClassLoader`_ is eccentric structure,enable useing application deploying to Agent. 
  In this case,If bypass ClassLoder configuation,Agent's local context ClassLoder is used.
  In this way,enable to use JobStreamer just job scheduler.
* Job's execution log is sent to Control bus by default,store Datomic.
* Depending on logback setting, be able to write log into local file of Agent or Control bus. 

.. _EDN Format: https://github.com/edn-format/edn
.. _WebSocketClassLoader: https://github.com/kawasima/websocket-classloader
.. highlight:: guess

Deploy batch components
===========

Example
--------------

1. Get Example::

   % git clone https://github.com/job-streamer/job-streamer-examples.git

2. Deploy it::

   % cd job-streamer-examples
   % mvn -e clean package job-streamer:deploy
  Deployed on control-bus.
  
  It needs that deploy resources and control bus are in same server.
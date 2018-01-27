==============
Limelight
==============
Limelight is a really cool camera that let's us do vision processing without much code at all.

Resources
=============
Limelight site: https://limelightvision.io/

Documentation: http://docs.limelightvision.io/en/latest/index.html

chiefdelphi thread: https://www.chiefdelphi.com/forums/showthread.php?t=160832&highlight=limelight

Programming the Limelight
=========================

.. code-block:: python

  from networktables import NetworkTables

  table = NetworkTables.getTable("limelight")
  tx = table.getNumber('tx',None)
  ty = table.getNumber('ty',None)
  ta = table.getNumber('ta',None)
  ts = table.getNumber('ts',None)
  
Limelight Dashboard
===================
To create your vision "pipeline" you need to access the limelight dashboard. You need safari or internet explorer to view the dashboard.

limelight dashboard: http://10.24.23.11:5801
camera stream: http://10.24.23.11:5800

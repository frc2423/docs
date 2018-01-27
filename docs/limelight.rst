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
  # Whether the limelight has any valid targets (0 or 1)
  tv = table.getNumber('tv',None)
  # Horizontal Offset From Crosshair To Target (-27 degrees to 27 degrees)
  tx = table.getNumber('tx',None)
  # Vertical Offset From Crosshair To Target (-20.5 degrees to 20.5 degrees)
  ty = table.getNumber('ty',None)
  # Target Area (0% of image to 100% of image)
  ta = table.getNumber('ta',None)
  # Skew or rotation (-90 degrees to 0 degrees)
  ts = table.getNumber('ts',None)
  
Limelight Dashboard
===================
To create your vision "pipeline" you need to access the limelight dashboard. You need safari or internet explorer to view the dashboard.

limelight dashboard: http://10.24.23.11:5801

camera stream: http://10.24.23.11:5800


Vision Target
=============

Information on the vision target is in section 3.9 of the game manual

  Vision targets are located on the SWITCH FENCE using 2 in. (~5 cm) strips of 3M 8830 Scotchlite
  Reflective Material and are used to highlight the locations of the PLATES on the SWITCH.
  
  **Each vision target consists of two vertical, 16 in. (~41 cm) tall strips of reflective material, with a 4 in.** (~10
  cm) gap between them. Elements of the SWITCH obscure the top and bottom of the target, resulting in
  approximately 15.3 in. (~39 cm) of viewable height when viewed straight on. The center of each target is
  located 51 7/8” in. (~132 cm) from the center of the SWITCH.

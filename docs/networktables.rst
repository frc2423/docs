=============
NetworkTables
=============

**NetworkTables resource**

`<http://robotpy.readthedocs.io/projects/pynetworktables/en/latest/api.html>`_
`<http://robotpy.readthedocs.io/projects/pynetworktables2js/en/stable/>`_

**Install NetworkTables**

Type these commands in the terminal:

.. code-block:: sh

   $ pip3 intall pynetworktables
   $ pip3 install pynetworktables2js


**What is NetworkTables?**

Joysticks give us an easy interface to control the robot, but what if we want to tell the robot where it's starting in the autonomous period? We can't use joysticks because we can't touch the conrols during the autonomous period. We can do this by building a webpage that aloows us to select the starting location before the match begins. The link that allows us to communicate between the webpage and robot is called NetworkTables. NetworkTables sends and receives data to the different devices on the robot network.

**NetworkTables on the robot**

To use NetworkTables on the robot we must import it just like we do with wpilib:

.. code-block:: Python

   from networktables import NetworkTables
   
Next we have to create a table. Tables contain the data we want to send back and forth between different devices during the match. For example, if we want to know where our robot is starting in autonomous mode, and if we're scoring a gear or just moving forward, we create an autonomous table. If we want to tell the webpage our robot's current heading and speed, we would have a sensor table:


.. code-block:: Python

   autonomousTable = NetworkTables.getTable("autonomous")
   sensorTable = NetworkTables.getTable("sensor")
   
To get the autonomous mode we would say:

.. code-block:: Python

   mode = autonomousTable.getString('mode', 'do_nothing')

If we want to tell the robot our current speed we would say:


.. code-block:: Python

    sensorTable.putNumber('speed', speed_sensor.getSpeed())


**NetworkTables on a webpage**

To use network tables on an HTML page we must have web server and a webpage. Go to where you have the robot repository in the terminal and type:

.. code-block:: sh

   $ git checkout networktables_fun
   $ git pull
   

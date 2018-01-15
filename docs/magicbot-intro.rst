============================
What is MagicBot?
============================

MagicBot is a framework that we'll be using to program our robot. Documentation can be found here:

http://robotpy.readthedocs.io/en/stable/frameworks/magicbot.html

http://robotpy-wpilib-utilities.readthedocs.io/en/latest/magicbot.html

Examples
==========

Just like IterativeRobot, MagicBot requires a few methods to work:

.. code-block:: python

  import magicbot
  import wpilib
  
  class MyRobot(magicbot.MagicRobot):

      def createObjects(self):
          '''Create motors and stuff here'''
          pass

      def teleopInit(self):
          '''Called when teleop starts; optional'''

      def teleopPeriodic(self):
          '''Called on each iteration of the control loop'''

  if __name__ == '__main__':
      wpilib.run(MyRobot)
      
Notice how we don't have a **robotInit** method to initialize motors and other objects. We do that inside and above the **createObjects** method.
      
A more detailed example can be found here: https://github.com/robotpy/examples/tree/master/magicbot-simple

Autonomous Modes
================

Notice in the example above there is no autonomous code? That's because all autonomous related code goes inside the *autonomous* folder next to the *robot.py* file. Each autonomous mode has its own file. MagicBot does the work of finding the autonomous modes, so we don't have to write any code in our robot.py file.

To select an autonomous mode on our dashboard, look at this example: https://github.com/robotpy/pynetworktables2js/blob/master/example/www/autonomous.html


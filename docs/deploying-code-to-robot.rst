============================
Deploying code to the robot
============================

Turning on the robot
====================

The first step to deploying code to the robot is to turn it on first. Make sure the battery is connected and tightly fastened to the robot. 

.. image:: images/deploying-code-to-robot/battery-disconnected.png

.. image:: images/deploying-code-to-robot/battery-connected.png

Next, turn on the robot by closing the black switch on the circuit breaker.

.. image:: images/deploying-code-to-robot/circuit-breaker-open.png

.. image:: images/deploying-code-to-robot/circuit-breaker-closed.png

Wait for the radio to power up
==============================

The radio - which allows us to communicate over a network and talk to the robot - must power up before we can deploy to the robot. Give the radio a minute to boot up before deploying code to the robot. 

This is what the radio looks like before it's fully booted:

.. image:: images/deploying-code-to-robot/radio-not-booted.png

This is what the radio looks like when it's fully booted:

.. image:: images/deploying-code-to-robot/radio-fully-booted.png

When the radio is powered up you should be able to connect to the robot's network:

.. image:: images/deploying-code-to-robot/robot-network.png


Writing a simple program to deploy to the robot
===============================================

 .. code-block:: python
 
  #!/usr/bin/env python3
  """
      This is a good foundation to build your robot code on
  """

  import wpilib

  class MyRobot(wpilib.TimedRobot):

      def robotInit(self):
          """
          This function is called upon program startup and
          should be used for any initialization code.
          """
          pass

      def autonomousInit(self):
          """This function is run once each time the robot enters autonomous mode."""
          pass

      def autonomousPeriodic(self):
          """This function is called periodically during autonomous."""
          pass

      def teleopPeriodic(self):
          """This function is called periodically during operator control."""
          pass

  if __name__ == "__main__":
      wpilib.run(MyRobot)
      
 Please refer to this page which breaks down how the above code works: https://robotpy.readthedocs.io/en/stable/guide/anatomy.html
 
Creating motor controllers
==========================


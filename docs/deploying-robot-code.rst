====================
Deploying Robot Code
====================
**Connect to the robot**

You must be first connected to the robot. Our wireless network should be 2423. The IP address of the router is 10.24.23.1 and the IP address of the robot is 10.24.23.2 or roborio-2423-frc.local. If you are having trouble deploying code troubleshoot by pinging these addresses:

.. code-block:: sh

   $ ping roborio-2423-frc.local
   $ ping 10.24.23.2
   $ ping 10.24.23.1


**Run the deploy command in the terminal**

Go to the terminal in the directory where you have your robot.py file. Type the following command (Note: if the command line doesn't like python try py or python3):

.. code-block:: sh

   $ python robot.py deploy --robot=[IP address of robot]

The IP address should be either *10.24.23.2* or *roborio-2423-frc.local*. If you don't have a robot available you can run this command to simulate the robot code:

.. code-block:: sh

   $ python robot.py sim

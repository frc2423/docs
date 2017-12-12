=============================
Setting Up Git
=============================

**What is git?**

Git is kind of like a google doc for code. It allows multiple people to make changes to our competition code and keeps track of changes (which is nice when there's a bug 

**Download git**

`<https://git-scm.com/downloads>`_

If you are using windows download git bash as well: `<https://git-for-windows.github.io/>`_

**Connecting to github**

You'll need to follow the steps in these links to push your code to the KwarQs repo:

`<https://help.github.com/articles/checking-for-existing-ssh-keys/>`_
`<https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/>`_
`<https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/>`_

Finally, go to our organization's github page and clone this year's repo to your computer: `<https://github.com/frc2423>`_





**Download the Java SDK**

You must have the Java SDK installed to use eclipse. Download it `here <http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html>`_. Choose the appropriate link under *Java SE Development Kit 8 Downloads*.


**Download Eclipse and Python**

Follow this guide to download the latest version of Eclipse and Python: `<http://www.mysamplecode.com/2012/10/python-tutorial-eclipse-pydev-plugin.html>`_

This guide also takes you through setting up a Python project in Eclipse. When you get to step 3, you can access the Eclipse update manager in the menu under *Help > Install New Software...*.


**Opening a file in the file manager or terminal/command line**

Follow the instructions to download the StartExplorer_ eclipse plugin.


.. _StartExplorer: http://basti1302.github.io/startexplorer/#screenshots


**Download Robot Python Packages**

After setting up Python types these commands inside the terminal/command prompt to get the Python packages required to write and deploy robot code:

.. code-block:: sh

   $ pip3 install pyfrc
   $ pip3 install robotpy-ctre

Bug fixes and other updates will be made to these packages, so at times you'll need to upgrade them:

.. code-block:: sh

   $ pip3 install pyfrc --upgrade
   $ pip3 install robotpy-ctre --upgrade

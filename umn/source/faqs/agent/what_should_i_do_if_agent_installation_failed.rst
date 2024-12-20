:original_name: hss_01_0069.html

.. _hss_01_0069:

What Should I Do If Agent Installation Failed?
==============================================

If this is the first time you install the agent, and the installation failed, rectify the fault by following the instructions provided in this section.

Symptoms
--------

The agent fails to be installed by running commands. The server list page on the console still indicates that the agent is not installed.

Possible Causes
---------------

-  The SELinux firewall has not been disabled.
-  The root account is not used for installation.
-  The installation command is incorrect.
-  Residual information exists after the agent is uninstalled.

Solution
--------

#. Check whether the SELinux firewall of the server is disabled.

   -  If it is, go to the next step.
   -  If it is not, disable it and install the agent again.

#. Check whether the installation command is suitable for the server region and OS.

   a. Switch to the server region.
   b. Copy the installation commands suitable for your server OS.

      -  Run 32-bit installation commands on a 32-bit server.
      -  Run 64-bit installation commands on a 64-bit server.

   -  If yes, go to the next step.
   -  If the commands you used are incorrect, install the agent again with correct ones.

#. Check whether the installation was performed by user **root**.

   -  If yes, go to the next step.
   -  If it was not, install the agent again as user **root**.

#. :ref:`Uninstall the agent <hss_01_0119>` as user **root** and forcibly install it.

   -  If the installation is successful, no further action is required.
   -  If the installation fails, contact technical support.

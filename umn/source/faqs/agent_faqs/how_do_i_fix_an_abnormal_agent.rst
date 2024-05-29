:original_name: hss_01_0036.html

.. _hss_01_0036:

How Do I Fix an Abnormal Agent?
===============================

Your agent is probably abnormal if it is in **Not installed** or **Offline** state. Agent statuses and their meaning are as follows:

-  **Uninstalled**: No agent has been installed on the server, or the agent has been installed but not started.
-  **Offline**: The communication between the agent and the server is abnormal. The agent on the server has been deleted, or a server is offline.
-  **Online**: The agent on the server is running properly.

Possible Causes
---------------

-  The agent status on the console is not updated.

   The agent status has not been updated. After the agent is installed, it takes 5 to 10 minutes for the console to update its status.

-  OS version not supported.

   For details, see "Constraints" in "Service Overview".

-  The network is faulty.

   The agent or the cloud protection center is abnormal. For example, the NIC is faulty, the IP address changes, or the bandwidth is low.

-  The agent process is abnormal.

Solution
--------

#. Check whether the agent status remains **Offline** on the console for more than 10 minutes after the agent was installed.

   -  If yes, go to :ref:`2 <hss_01_0036__li1862125342316>`.
   -  If no, wait until the agent goes online. No further action is required. After the agent was installed, it takes 5 to 10 minutes for the console to update its status.

#. .. _hss_01_0036__li1862125342316:

   Check whether your server OS is within the scope of support in "Constraints" in "Service Overview".

   -  If yes, go to :ref:`3 <hss_01_0036__li1040605463416>`.
   -  If no, the HSS agent cannot be installed or run on your server. Upgrade the OS to a version supported by HSS and try again.

#. .. _hss_01_0036__li1040605463416:

   Check whether the server network is normal.

   -  If yes, go to :ref:`4 <hss_01_0036__li64084228240>`.
   -  If no, After the server can access the network, check the agent status.

#. .. _hss_01_0036__li64084228240:

   Restart the agent process.

   -  Windows

      a. Log in to the server as user **administrator**.
      b. Open the Task Manager.
      c. On the **Services** tab page, select **HostGuard**.
      d. Right-click the service and choose **Restart**.

   -  Linux

      Run the following command in the CLI as user **root** to restart the agent:

      **service hostguard restart**

      If the following information is displayed, the restart is successful:

      .. code-block::

         root@HSS-Ubuntu32:~#service hostguard restart
         Stopping Hostguard...
         Hostguard stopped
         Hostguard restarting...
         Hostguard is running

   After the process is restarted, wait for about 2 minutes.

   -  If the agent status is **Online**, no further action is required.
   -  If the agent status is still **Not installed** or **Offline**, uninstall the agent and install it again.

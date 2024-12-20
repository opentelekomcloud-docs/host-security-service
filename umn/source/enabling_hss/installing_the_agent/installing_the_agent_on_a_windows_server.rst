:original_name: hss_01_0648.html

.. _hss_01_0648:

Installing the Agent on a Windows Server
========================================

You can enable HSS for ECSs only after installing the agent. This section describes how to install the agent on a Windows server.

Prerequisites
-------------

-  The server is running.
-  Ensure the outbound rule of your security group allows access to the port 10180 on the 100.125.0.0/16 network segment. (This is the default setting.)
-  The available capacity of the disk where the agent is to be installed must be greater than 300 MB. Otherwise, the agent installation may fail.
-  If any third-party security software has been installed on your server, the HSS agent may fail to be installed. In this case, disable or uninstall the software before installing the agent.

Constraints
-----------

Only 64-bit server protection is supported.

Installation Path
-----------------

The agent installation path on servers running on Windows cannot be customized. The default path is: **C:\\Program Files\\HostGuard**.

Procedure
---------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane, choose **Installation & Configuration**.

#. Click the **Agent Management** tab.

#. Copy the address for downloading the agent installation package.

   a. Click the value of **Servers Without Agents** area to filter the servers that have not installed agents.
   b. In the **Operation** column of a server, click **Install Agent**.
   c. In the displayed dialog box, click **Copy** to copy the address for downloading the agent installation package.

#. Remotely log in as user **Administrator** to the server where the agent is to be installed.

#. On the server where the agent is to be installed, use Internet Explorer to download the agent installation package from the copied agent download address and decompress it.

#. Run the agent installation program.

#. Check the **HostGuard.exe** and **HostWatch.exe** processes in the Windows Task Manager.

   If the processes do not exist, the agent installation fails. In this case, reinstall the agent. It takes 3 to 5 minutes for the console to update the agent status after agent installation.

Follow-up Procedure
-------------------

After the agent is installed, enable security protection for your server. For details, see :ref:`Enabling Protection <hss_01_0260>`.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

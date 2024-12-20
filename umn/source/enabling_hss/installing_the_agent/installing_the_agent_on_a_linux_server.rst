:original_name: hss_01_0609.html

.. _hss_01_0609:

Installing the Agent on a Linux Server
======================================

You can enable HSS for ECSs only after installing the agent. This section describes how to install the agent on a Linux server.

Prerequisites
-------------

-  The server is running.
-  Ensure the outbound rule of your security group allows access to the port 10180 on the 100.125.0.0/16 network segment. (This is the default setting.)
-  The available capacity of the disk where the agent is installed must be greater than 300 MB. Otherwise, the agent installation may fail.
-  The Security-Enhanced Linux (SELinux) firewall has been disabled. The firewall affects agent installation and should remain disabled until the agent is installed.
-  If any third-party security software has been installed on your server, the HSS agent may fail to be installed. In this case, disable or uninstall the software before installing the agent.

Constraints
-----------

Only 64-bit server protection is supported.

Installation Path
-----------------

The agent installation path on servers running on Linux cannot be customized. The default path is: **/usr/local/hostguard/**.

Procedure
---------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane, choose **Installation & Configuration**.

#. Click the **Agent Management** tab.

#. Copy the command for installing the agent.

   a. Click the value of **Servers Without Agents** area to filter the servers that have not installed agents.
   b. In the **Operation** column of a server, click **Install Agent**.
   c. In the displayed dialog box, click **Copy**.

#. Remotely log in as user **root** to the server where the agent is to be installed.

#. Run the copied installation command to install the agent.

   If the command output shown in :ref:`Installation completed <hss_01_0609__fig7475843113413>` is displayed, the agent is successfully installed.

   .. _hss_01_0609__fig7475843113413:

   .. figure:: /_static/images/en-us_image_0000001773082761.png
      :alt: **Figure 1** Installation completed

      **Figure 1** Installation completed

#. Run the following command to check the runtime status of agent:

   **service hostguard status**

   If the command output shown in :ref:`Agent running properly <hss_01_0609__fig109291726183713>` is displayed, the agent is running properly.

   .. _hss_01_0609__fig109291726183713:

   .. figure:: /_static/images/en-us_image_0000001773088597.png
      :alt: **Figure 2** Agent running properly

      **Figure 2** Agent running properly

   After the installation, it takes 5 to 10 minutes to update the agent status. You can check it on the **Servers** tab of the **Asset Management** > **Servers & Quota** page.

Follow-up Procedure
-------------------

After the agent is installed, enable security protection for your server. For details, see :ref:`Enabling Protection <hss_01_0260>`.

.. |image1| image:: /_static/images/en-us_image_0000001708541240.png

:original_name: hss_01_0293.html

.. _hss_01_0293:

Viewing the Container Node Protection Status
============================================

The **Container Nodes** page displays the protection, node, and agent status of containers, helping you learn the node security status in real time.

Constraints
-----------

-  Only Linux servers are supported.
-  Servers that are not protected by HSS enterprise, premium, WTP, or container editions cannot perform container-related operations.


Viewing the Container Node Protection Status
--------------------------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane on the left, choose **Asset Management** > **Containers & Quota**. Click **Container Nodes**.

#. View the node protection status on the **Nodes** page. You can obtain the details in :ref:`Table 1 <hss_01_0293__table13936165011391>`.

   .. note::

      In the HSS container node list, you can view only the servers where the agent has been installed. To view the servers where the agent has not been installed, choose **Asset Management** > **Servers & Quota**.

   .. _hss_01_0293__table13936165011391:

   .. table:: **Table 1** Parameter description

      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                   |
      +===================================+===============================================================================================================================================================+
      | Server Information                | Server name and IP address. Move the cursor over to the server name to view the server details, including the server ID, OS, system name, and system version. |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Protection Status                 | Protection status of a node. The options are as follows:                                                                                                      |
      |                                   |                                                                                                                                                               |
      |                                   | -  **Unprotected**: HSS is disabled for the server. After the agent is installed, click **Enable** in the **Operation** column to enable protection.          |
      |                                   | -  **Enabled**: The server is fully protected by HSS.                                                                                                         |
      |                                   | -  **Protection interrupted**: The server is shut down, the agent is offline, or the agent is uninstalled.                                                    |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Server Status                     | -  Running                                                                                                                                                    |
      |                                   | -  Unavailable                                                                                                                                                |
      |                                   | -  Normal                                                                                                                                                     |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Agent Status                      | You can select a status to view the server.                                                                                                                   |
      |                                   |                                                                                                                                                               |
      |                                   | -  **Online**: The agent is running properly.                                                                                                                 |
      |                                   | -  **Offline**: The communication between the agent and the HSS server is abnormal, and HSS cannot protect your servers.                                      |
      |                                   | -  **Not installed**: The agent has not been installed or successfully started.                                                                               |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

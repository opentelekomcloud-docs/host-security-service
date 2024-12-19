:original_name: hss_01_0649.html

.. _hss_01_0649:

Batch Installing Agents on Linux Servers
========================================

HSS allows you to install agents for Linux servers in batches. Agents cannot be installed on Windows servers in batches.

Prerequisite
------------

-  The server is running.
-  Ensure the outbound rule of your security group allows access to the port 10180 on the 100.125.0.0/16 network segment. (This is the default setting.)
-  The available capacity of the disk where the agent is installed must be greater than 300 MB. Otherwise, the agent installation may fail.
-  The Security-Enhanced Linux (SELinux) firewall has been disabled. The firewall affects agent installation and should remain disabled until the agent is installed.
-  If any third-party security software has been installed on your server, the HSS agent may fail to be installed. In this case, disable or uninstall the software before installing the agent.

-  The server supports SSH login.

Installation Path
-----------------

The agent installation path on servers running on Linux cannot be customized. The default path is: **/usr/local/hostguard/**.

Installing Agents in Batches on the Console
-------------------------------------------

**Scenario**

You can install agents in batches on the console only if the following conditions are met:

-  There are fewer than 50 servers waiting for agent installation, and the accounts and passwords of these servers are the same.
-  There is a server with an online agent in the VPC of the servers where the agent is to be installed. If there is no online agent server, install an agent on a server by referring to :ref:`Installing the Agent on a Linux Server <hss_01_0609>`.

**Procedure**

#. Log in to the management console.
#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

3. In the navigation pane, choose **Asset Management** > **Servers & Quota**. Click the **Servers** tab.

4. Select all target servers and click **Install Agent** above the server list.

5. Enter the server root password and server login port.

   .. note::

      -  The default system port is **22**. To query the Linux SSH port, remotely log in to the target server and run the following command on the Linux server:

         .. code-block::

            cat /etc/ssh/sshd_config | grep Port

      -  If the server password contains the character **$**, enter **\\$**.

6. Click **OK**. Agents will be automatically installed on the servers you selected.

   Agents will be automatically installed on the servers you selected in sequence. You can choose **Asset Management** > **Servers & Quota** and click the **Servers** tab to view agent status. If the **Agent Status** of a target server changes to **Online**, you can enable protection for the server.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

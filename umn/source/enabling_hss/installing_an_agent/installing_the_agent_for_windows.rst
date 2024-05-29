:original_name: hss_01_0236.html

.. _hss_01_0236:

Installing the Agent for Windows
================================

You can enable HSS only after the agent is installed on your servers. This topic describes how to install the agent on a server running a Windows OS. For details about how to install an agent on the Linux OS, see :ref:`Installing an Agent on Linux <hss_01_0571>`.

Default Installation Path
-------------------------

The agent installation path on servers running the Windows OS cannot be customized. The default path is:

**C:\\Program Files\\HostGuard**

Precaution
----------

If you uninstall an agent and install it again on a Windows server, the message "Installation failed" will probably be displayed. This is a misreport and you can ignore it.

Prerequisite
------------

-  The server runs Windows OS.
-  A remote management tool, such as pcAnywhere and UltraVNC, has been installed on your PC.

Procedure
---------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

#. In the navigation pane, choose **Installation & Configuration**. Click the **Agents** tab. Click **Offline**.


   .. figure:: /_static/images/en-us_image_0000001563539818.png
      :alt: **Figure 1** Accessing the agent management page

      **Figure 1** Accessing the agent management page

#. .. _hss_01_0236__li1339342620496:

   In the **Operation** column of the server, click **Install Agent** to obtain the link for downloading the agent installation script.

#. Remotely log in to the server where the agent is to be installed.

   -  You can log in to the ECS management console and click **Remote Login** in the ECS list.
   -  If an EIP has been bound to the server, you can log in to the server by using Windows Remote Desktop Connection or a third-party remote management tool, such as pcAnywhere or UltraVNC.

#. On the server where the agent is to be installed, open the link obtained in :ref:`4 <hss_01_0236__li1339342620496>` by using the Internet Explorer. Download the agent installation script.

#. Run the agent installation script as the administrator.

#. Check the **HostGuard.exe** and **HostWatch.exe** processes in the Windows Task Manager.

   If the processes do not exist, the agent installation fails. In this case, reinstall the agent.

.. |image1| image:: /_static/images/en-us_image_0000001568517705.png

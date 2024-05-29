:original_name: hss_01_0571.html

.. _hss_01_0571:

Installing an Agent on Linux
============================

To enable workload protection for cloud servers, install the agent first.

This topic describes how to install the agent on a server running Linux.

.. note::

   CentOS 6.x is no longer updated or maintained on the Linux official website, and HSS no longer supports CentOS 6.x or earlier.

Default Installation Path
-------------------------

The agent installation path on servers running the Linux OS cannot be customized. The default path is:

**/usr/local/hostguard/**

Prerequisites
-------------

-  To install the agent on a server on another cloud, ensure the server runs Linux and can access the Internet.
-  The Security-Enhanced Linux (SELinux) firewall has been disabled. The firewall affects agent installation and should remain disabled until the agent is installed.

Installation Precautions
------------------------

-  For details about the OSs supported by the agent, see :ref:`Supported OSs <hss_01_0137__section3897426874>`.

-  Ensure the outbound rule of your security group allows access to the port 10180 on the 100.125.0.0/16 network segment. (This is the default setting.)
-  If any third-party security software has been installed on your server, the HSS agent may fail to be installed. In this case, disable or uninstall the software before installing the agent.
-  The available capacity of the disk where the agent is installed must be greater than 300 MB. Otherwise, the agent installation may fail.
-  After the installation, it takes 5 to 10 minutes to update the agent status. You can check it on the "Servers" tab of the "Asset Management > Servers & Quota" page.

Installing an Agent Using Commands
----------------------------------

This procedure involves logging in to the server and running commands. It takes 3 to 5 minutes for the console to update the agent status after agent installation.

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

#. In the navigation pane, choose **Installation & Configuration**.

#. Click the **Agents** tab. Click **Offline**. In the **Operation** column of a server, click **Install Agent**.


   .. figure:: /_static/images/en-us_image_0000001563116264.png
      :alt: **Figure 1** Installing an Agent

      **Figure 1** Installing an Agent

#. In the displayed dialog box, copy the command suitable for your system architecture and OS.

#. Remotely log in to the server where the agent is to be installed.

   -  You can log in to the ECS management console and click **Remote Login** in the ECS list.
   -  If your server has an EIP bound, you can also use a remote management tool, such as Xftp, SecureFX, WinSCP, PuTTY, or Xshell, to log in to the server and install the agent on the server as user **root**.

#. Paste the copied installation command and run it as user **root** to install the agent on the server.

   If information similar to the following is displayed, the agent is successfully installed:

   .. code-block::

      Preparing...                  ########################## [100%]
      1:hostguard                   ########################## [100%]
      Hostguard is running.
      Hostguard installed.

#. Run the **service hostguard status** command to check the running status of the agent.

   If the following information is displayed, the agent is running properly:

   .. code-block::

      Hostguard is running

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

:original_name: hss_01_0480.html

.. _hss_01_0480:

Viewing Plug-in Information
===========================

The plug-in configuration page displays the server list and the plug-in information of the servers. If no plug-ins are installed on a server, the corresponding plug-in information is empty. You can view the plug-in information of a server to determine the servers where plug-ins need to be installed.


Viewing Plug-in Information
---------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane on the left, choose **Installation & Configuration** > **Plug-in Settings**. View plug-in details on the plug-in settings page. For more information, see :ref:`Table 1 <hss_01_0480__table88301641142619>`.

   By default, all servers are displayed in the plug-in list. If a plug-in is installed on a server, the plug-in details are displayed. If no plug-ins are installed on a server, the plug-in information is empty.

   .. _hss_01_0480__table88301641142619:

   .. table:: **Table 1** Docker plug-in list parameters

      +-----------------------------------+-------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                   |
      +===================================+===============================================================================+
      | Server Name/ID                    | Server name and ID                                                            |
      +-----------------------------------+-------------------------------------------------------------------------------+
      | IP Address                        | Server IP address                                                             |
      +-----------------------------------+-------------------------------------------------------------------------------+
      | OS                                | Type of the OS running on the server                                          |
      +-----------------------------------+-------------------------------------------------------------------------------+
      | Plug-in Name                      | Name of the plug-in installed on the server.                                  |
      +-----------------------------------+-------------------------------------------------------------------------------+
      | Plug-in Version                   | Name of the plug-in installed on the server.                                  |
      +-----------------------------------+-------------------------------------------------------------------------------+
      | Plug-in Status                    | Current status of the plug-in.                                                |
      |                                   |                                                                               |
      |                                   | -  **Created**: The plug-in has been created but has not been started.        |
      |                                   | -  **Running**: The plug-in is running properly.                              |
      |                                   | -  **Paused**: The plug-in is paused.                                         |
      |                                   | -  **Restarting**: The plug-in is being restarted.                            |
      |                                   | -  **Removing**: The plug-in is being deleted.                                |
      |                                   | -  **Exited**: The plug-in has been stopped.                                  |
      |                                   | -  **Dead**: The plug-in cannot be started or has been deleted.               |
      +-----------------------------------+-------------------------------------------------------------------------------+
      | Plug-in Upgrade Status            | Plug-in upgrade status.                                                       |
      |                                   |                                                                               |
      |                                   | -  **Not upgraded**: The plug-in has not been upgraded to the latest version. |
      |                                   | -  **Upgrading**: The plug-in is being upgraded.                              |
      |                                   | -  **Upgraded**: The plug-in has been upgraded.                               |
      |                                   | -  **Upgrade failed**: The plug-in failed to be upgraded.                     |
      +-----------------------------------+-------------------------------------------------------------------------------+

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

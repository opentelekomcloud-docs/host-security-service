:original_name: hss_01_0570.html

.. _hss_01_0570:

Installing an Agent
===================

Install the agent on a server. Only then can the server be protected by HSS.

Installing an Agent on a Server
-------------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

#. In the navigation pane, choose **Installation & Configuration**. Click the **Agents** tab.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.


   .. figure:: /_static/images/en-us_image_0000001670681801.png
      :alt: **Figure 1** Viewing agent management

      **Figure 1** Viewing agent management

#. Click **Offline** to check the servers where the agent is not installed or is offline. :ref:`Table 1 <hss_01_0570__table1926618704616>` describes the parameters.

   .. _hss_01_0570__table1926618704616:

   .. table:: **Table 1** Offline agent parameters

      +-----------------------------------+---------------------------------------------+
      | Parameter                         | Description                                 |
      +===================================+=============================================+
      | Server Name/ID                    | Server name and ID                          |
      +-----------------------------------+---------------------------------------------+
      | IP Address                        | EIP or private IP address of a server       |
      +-----------------------------------+---------------------------------------------+
      | OS                                | Server OS. Its value can be:                |
      |                                   |                                             |
      |                                   | -  **Linux**                                |
      |                                   | -  **Windows**                              |
      +-----------------------------------+---------------------------------------------+
      | Agent Status                      | Agent status of a server. Its value can be: |
      |                                   |                                             |
      |                                   | -  **Offline**                              |
      |                                   | -  **Not installed**                        |
      |                                   | -  **Installation failed**                  |
      +-----------------------------------+---------------------------------------------+

#. Click **View Cause** in the **Operation** column of a server to check why an agent is offline.

#. Click **Install Agent** in the **Operation** column. Download the agent package suitable for your server architecture and OS. For details about how to install the agent on a Linux server, see :ref:`Installing an Agent on Linux <hss_01_0571>`. For details about how to install the agent on a Windows server, see :ref:`Installing the Agent for Windows <hss_01_0236>`.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

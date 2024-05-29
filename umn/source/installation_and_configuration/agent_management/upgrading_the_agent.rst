:original_name: hss_01_0462.html

.. _hss_01_0462:

Upgrading the Agent
===================

HSS keeps improving its service capabilities, including but not limited to new features and defect fixes. Please upgrade your agent to the latest version in a timely manner to enjoy better service.

Upgrading the Agent on a Single Server
--------------------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

#. In the navigation pane, choose **Installation & Configuration**. Click the **Agents** tab.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.


   .. figure:: /_static/images/en-us_image_0000001670681801.png
      :alt: **Figure 1** Viewing agent management

      **Figure 1** Viewing agent management

#. Click **Online** to view the list of servers where the agent has been installed. For details, see :ref:`Table 1 <hss_01_0462__table1470654415335>`.

   .. _hss_01_0462__table1470654415335:

   .. table:: **Table 1** Online agent parameters

      +-----------------------------------+---------------------------------------------+
      | Parameter                         | Description                                 |
      +===================================+=============================================+
      | Server Name/ID                    | Server name and ID                          |
      +-----------------------------------+---------------------------------------------+
      | IP Address                        | EIP or private IP address of a server       |
      +-----------------------------------+---------------------------------------------+
      | OS                                | Server OS. Its value can be:                |
      |                                   |                                             |
      |                                   | -  Linux                                    |
      |                                   | -  Windows                                  |
      +-----------------------------------+---------------------------------------------+
      | Agent status                      | Agent status of a server. Its value can be: |
      |                                   |                                             |
      |                                   | -  **Online**                               |
      +-----------------------------------+---------------------------------------------+

#. Click **Upgrade** in the **Operation** column of the target server. In the dialog box displayed, confirm the upgrade details and click **OK**.

#. After the upgrade completes, check the agent version. If the latest version agent is used, the upgrade is successful.

Upgrading the Agent on Multiple Servers
---------------------------------------

#. Log in to the management console.

#. In the navigation pane, choose **Installation & Configuration**. Click the **Agents** tab.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.


   .. figure:: /_static/images/en-us_image_0000001670681801.png
      :alt: **Figure 2** Viewing agent management

      **Figure 2** Viewing agent management

#. Click **Online** to view the list of servers where the agent has been installed. For details, see :ref:`Table 2 <hss_01_0462__hss_01_0462_table1470654415335>`.

   .. _hss_01_0462__hss_01_0462_table1470654415335:

   .. table:: **Table 2** Online agent parameters

      +-----------------------------------+---------------------------------------------+
      | Parameter                         | Description                                 |
      +===================================+=============================================+
      | Server Name/ID                    | Server name and ID                          |
      +-----------------------------------+---------------------------------------------+
      | IP Address                        | EIP or private IP address of a server       |
      +-----------------------------------+---------------------------------------------+
      | OS                                | Server OS. Its value can be:                |
      |                                   |                                             |
      |                                   | -  Linux                                    |
      |                                   | -  Windows                                  |
      +-----------------------------------+---------------------------------------------+
      | Agent status                      | Agent status of a server. Its value can be: |
      |                                   |                                             |
      |                                   | -  **Online**                               |
      +-----------------------------------+---------------------------------------------+

#. Select the target servers whose agent you want to upgrade.

   .. note::

      -  If you check the box before **Server Name/ID**, all servers on the page will be selected.
      -  If you check the box before **Select all**, all servers you have will be selected.


   .. figure:: /_static/images/en-us_image_0000001622204562.png
      :alt: **Figure 3** Selecting all servers whose agent needs to be upgraded

      **Figure 3** Selecting all servers whose agent needs to be upgraded

#. Click **Upgrade Agent** above the server list. In the dialog box displayed, confirm server information and click **OK**.

#. After the upgrade completes, check the agent version. If the latest version agent is used, the upgrade is successful.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

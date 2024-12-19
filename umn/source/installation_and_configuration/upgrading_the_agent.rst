:original_name: hss_01_0462.html

.. _hss_01_0462:

Upgrading the Agent
===================

HSS keeps improving its service capabilities, including but not limited to new features and defect fixes. Please upgrade your agent to the latest version in a timely manner to enjoy better service.

Manually Upgrading the Agent
----------------------------

#. Log in to the management console.

#. In the navigation pane, choose **Installation & Configuration**. Click the **Agents** tab.

   .. note::

      If your servers are managed by enterprise projects, you can select the target enterprise project to view or operate the asset and detection information.

#. Click **Agents to Be Upgraded** and filter the servers whose agents are to be upgraded.

#. In the **Operation** column of a server, click **Upgrade Agent**.

   You can also select target servers in batches and click **Upgrade Agent** in the upper left corner of the server list to upgrade agents for the servers in batches.

#. In the displayed dialog box, confirm the server whose agent is to be upgraded and click **OK** to start the automatic upgrade.

#. After the upgrade completes, check the agent version. If the latest version agent is used, the upgrade is successful.

Automatically Upgrading Agents
------------------------------

#. Log in to the management console.

#. In the navigation pane, choose **Installation & Configuration**. Click the **Agents** tab.

   .. note::

      If your servers are managed by enterprise projects, you can select the target enterprise project to view or operate the asset and detection information.

#. Click |image1| to enable automatic agent upgrade.

   After this function is enabled, HSS checks the agent to be upgraded from 00:00 to 06:00 every day and automatically upgrades the agent to the latest version.

   .. note::

      The automatic upgrade can be performed only when the agent status is **Online**.

.. |image1| image:: /_static/images/en-us_image_0000001929239225.png

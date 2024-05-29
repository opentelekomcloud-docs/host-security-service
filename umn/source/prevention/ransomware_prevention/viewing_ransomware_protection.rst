:original_name: hss_01_0347.html

.. _hss_01_0347:

Viewing Ransomware Protection
=============================

Prerequisites
-------------

You have enabled HSS premium, WTP, or container edition.

Constraints
-----------

-  After ransomware protection is enabled, you need to handle ransomware alarms and fix the vulnerabilities in your systems and middleware in a timely manner.

Checking the Ransomware Prevention Overview
-------------------------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

#. In the navigation pane, choose **Prevention** > **Ransomware Prevention**. Check ransomware prevention details.


   .. figure:: /_static/images/en-us_image_0000001808126138.png
      :alt: **Figure 1** Ransomware prevention overview

      **Figure 1** Ransomware prevention overview

   .. table:: **Table 1** Ransomware prevention parameters

      +-----------------------+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------+
      | Parameter             |                                | Description                                                                                                                                                                                                                          | Example Value            |
      +=======================+================================+======================================================================================================================================================================================================================================+==========================+
      | Enterprise Project    |                                | After an enterprise project is selected, the overview page will display the data in the project only.                                                                                                                                | ``-``                    |
      |                       |                                |                                                                                                                                                                                                                                      |                          |
      |                       |                                | You can select an existing enterprise project. By default, data of all servers is displayed.                                                                                                                                         |                          |
      +-----------------------+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------+
      | Time range            |                                | Select a time range to check ransomware defense statistics.                                                                                                                                                                          | Last 30 days             |
      |                       |                                |                                                                                                                                                                                                                                      |                          |
      |                       |                                | Valid values: **Last 24 hours**, **Last 3 days**, **Last 7 days**, **Last 30 days**                                                                                                                                                  |                          |
      +-----------------------+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------+
      | Protection Statistics | Protected Servers              | Number of servers protected against ransomware.                                                                                                                                                                                      | ``-``                    |
      +-----------------------+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------+
      |                       | Events                         | Number of ransomware-related events detected within the specified time range.                                                                                                                                                        | ``-``                    |
      +-----------------------+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------+
      | Backup Statistics     | Backed Up Servers              | Number of servers whose data has been backed up.                                                                                                                                                                                     | ``-``                    |
      +-----------------------+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------+
      |                       | Backup and Restoration Tasks   | Number of server data restoration tasks. You can click the number to view the task progress.                                                                                                                                         | ``-``                    |
      +-----------------------+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------+
      | Protected Servers     | Server Name/ID                 | Server name and ID. You can click a server name to view its details.                                                                                                                                                                 | ``-``                    |
      +-----------------------+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------+
      |                       | IP Address                     | EIP and private IP address of a server.                                                                                                                                                                                              | ``-``                    |
      +-----------------------+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------+
      |                       | OS                             | Server OS.                                                                                                                                                                                                                           | Linux                    |
      +-----------------------+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------+
      |                       | Server Status                  | Server status. It can be:                                                                                                                                                                                                            | ``-``                    |
      |                       |                                |                                                                                                                                                                                                                                      |                          |
      |                       |                                | -  **Running**                                                                                                                                                                                                                       |                          |
      |                       |                                | -  **Stopped**                                                                                                                                                                                                                       |                          |
      +-----------------------+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------+
      |                       | Ransomware Protection Status   | Ransomware protection status of a server. Its value can be:                                                                                                                                                                          | Enabled                  |
      |                       |                                |                                                                                                                                                                                                                                      |                          |
      |                       |                                | -  **Enabling**                                                                                                                                                                                                                      |                          |
      |                       |                                | -  **Enabled**                                                                                                                                                                                                                       |                          |
      |                       |                                | -  **Disabling**                                                                                                                                                                                                                     |                          |
      |                       |                                | -  **Disabled**                                                                                                                                                                                                                      |                          |
      +-----------------------+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------+
      |                       | Policy                         | Policy used for the server.                                                                                                                                                                                                          | ``-``                    |
      +-----------------------+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------+
      |                       | Events                         | Number of events detected within the selected time range.                                                                                                                                                                            | ``-``                    |
      +-----------------------+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------+
      |                       | Backup Status                  | Status of the backup function. Its value can be:                                                                                                                                                                                     | Enabled                  |
      |                       |                                |                                                                                                                                                                                                                                      |                          |
      |                       |                                | -  **Enabled**: Automatic full data backup has been enabled for a server.                                                                                                                                                            |                          |
      |                       |                                | -  **Disabled**: Automatic full data backup is disabled for a server.                                                                                                                                                                |                          |
      +-----------------------+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------+
      |                       | Backup Policy Status           | Status of the backup policy associated with the target server                                                                                                                                                                        | **Enabled**              |
      +-----------------------+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------+
      |                       | Vault Status                   | Status of the vault associated with the backup on the target server                                                                                                                                                                  | **Available**            |
      +-----------------------+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------+
      |                       | Associated Vault               | Name of the vault bound to the target server                                                                                                                                                                                         | ``-``                    |
      +-----------------------+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------+
      |                       | Bound Servers                  | Number of servers associated with the backup vault                                                                                                                                                                                   | 3                        |
      +-----------------------+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------+
      |                       | Used/Total Vault Capacity (GB) | The used capacity and total capacity of the vault associated with the target server                                                                                                                                                  | 30/400                   |
      +-----------------------+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------+
      |                       | Backups                        | Number of backups generated in the vault                                                                                                                                                                                             | 18                       |
      +-----------------------+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------+
      | Policies              | Policy                         | Policy name.                                                                                                                                                                                                                         | ``-``                    |
      +-----------------------+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------+
      |                       | Action                         | Action of a policy. Its value can be:                                                                                                                                                                                                | Report alarm and isolate |
      |                       |                                |                                                                                                                                                                                                                                      |                          |
      |                       |                                | -  **Report alarm**: If a virus is detected, an alarm will be reported.                                                                                                                                                              |                          |
      |                       |                                | -  **Report alarm and isolate**: If a virus is detected, an alarm will be reported and the virus will be isolated.                                                                                                                   |                          |
      +-----------------------+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------+
      |                       | Bait File                      | Files and directories that store invalid data on servers and are used as bait files.                                                                                                                                                 | Enabled                  |
      |                       |                                |                                                                                                                                                                                                                                      |                          |
      |                       |                                | If ransomware prevention is enabled, this function is enabled by default.                                                                                                                                                            |                          |
      |                       |                                |                                                                                                                                                                                                                                      |                          |
      |                       |                                | After bait file is enabled, the system deploys bait files in protected directories and key directories (unless otherwise specified by users). A bait file occupies only a few resources and does not affect your server performance. |                          |
      +-----------------------+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------+
      |                       | OS                             | OS of the server to which the target policy is bound.                                                                                                                                                                                | Windows                  |
      +-----------------------+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------+
      |                       | Associated Servers             | Number of servers associated with the policy.                                                                                                                                                                                        | ``-``                    |
      +-----------------------+--------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------+

Viewing Backup and Restoration Tasks
------------------------------------

.. important::

   The backup of HSS ransomware protection depends on Cloud Backup and Recovery (CBR). Before enabling server backup, ensure that you have applied for CBR.

#. Log in to the management console and go to the HSS page.

#. In the navigation pane, choose **Prevention** > **Ransomware Prevention**. Click the number of backup and restoration tasks.

#. In the dialog box that is displayed, view the backup and restoration task details. You can filter or search for a server by its name or status. For more information, see :ref:`Table 2 <hss_01_0347__table88217551915>`.

   .. _hss_01_0347__table88217551915:

   .. table:: **Table 2** Backup and restoration task parameters

      +-----------------------+-------------------------------------------------------------------------+-----------------------+
      | Parameter             | Description                                                             | Example Value         |
      +=======================+=========================================================================+=======================+
      | Server Name/ID        | Name or ID of a server that executes a restoration task.                | ``-``                 |
      +-----------------------+-------------------------------------------------------------------------+-----------------------+
      | Backup Name           | Name of a backup file.                                                  | ``-``                 |
      +-----------------------+-------------------------------------------------------------------------+-----------------------+
      | Restoration Status    | Restoration status of a server. It can be:                              | Succeeded             |
      |                       |                                                                         |                       |
      |                       | -  **Succeeded**                                                        |                       |
      |                       | -  **Skipped**                                                          |                       |
      |                       | -  **Failed**                                                           |                       |
      |                       | -  **In progress**                                                      |                       |
      |                       | -  **Timed out**                                                        |                       |
      |                       | -  **Waiting**                                                          |                       |
      |                       |                                                                         |                       |
      |                       | If a task was skipped, failed, or timed out, perform restoration again. |                       |
      +-----------------------+-------------------------------------------------------------------------+-----------------------+
      | Start/End Time        | Start and end time of backup and restoration.                           | ``-``                 |
      +-----------------------+-------------------------------------------------------------------------+-----------------------+

Restoring Server Data
---------------------

.. important::

   The backup of HSS ransomware protection depends on Cloud Backup and Recovery (CBR). Before enabling server backup, ensure that you have applied for CBR.

#. Log in to the management console and go to the HSS page.

#. In the navigation pane, choose **Prevention** > **Ransomware Prevention**. Click the **Protected Servers** tab. In the **Operation** column of the target server, click **More** > **Restore Data**.

#. In the dialog box that is displayed, view information about the server to be restored. You can search for the backup data source to be restored by filtering the backup status and searching for the backup name. For more information, see :ref:`Table 3 <hss_01_0347__table17472183015292>`.

   .. _hss_01_0347__table17472183015292:

   .. table:: **Table 3** Backup data source parameters

      +-----------------------+----------------------------------------------------------------------------------------------------------+-----------------------+
      | Parameter             | Description                                                                                              | Example Value         |
      +=======================+==========================================================================================================+=======================+
      | Backup Name           | Name of a backup file.                                                                                   | ``-``                 |
      +-----------------------+----------------------------------------------------------------------------------------------------------+-----------------------+
      | Status                | Backup status. It can be:                                                                                | Available             |
      |                       |                                                                                                          |                       |
      |                       | -  **Available**                                                                                         |                       |
      |                       | -  **Creating**                                                                                          |                       |
      |                       | -  **Deleting**                                                                                          |                       |
      |                       | -  **Restoring**                                                                                         |                       |
      |                       | -  **Error**                                                                                             |                       |
      |                       |                                                                                                          |                       |
      |                       | A backup in **Available** state can be used for restoration.                                             |                       |
      +-----------------------+----------------------------------------------------------------------------------------------------------+-----------------------+
      | Purpose               | Backup purpose. It can be:                                                                               | Periodic execution    |
      |                       |                                                                                                          |                       |
      |                       | -  **Periodic execution**: Data is backed up based on the backup period configured in the backup policy. |                       |
      |                       | -  **Ransomware protection**: Data is backed up immediately when a server is attacked by ransomware.     |                       |
      +-----------------------+----------------------------------------------------------------------------------------------------------+-----------------------+
      | Execution Time        | Time when the data source was backed up.                                                                 | ``-``                 |
      +-----------------------+----------------------------------------------------------------------------------------------------------+-----------------------+

#. In the **Operation** column of a backup, click **Restore Data**.

   .. note::

      Only a backup in the available state can be restored.

#. In the dialog box that is displayed, confirm the server information and click **OK**.

Modifying a Backup Policy
-------------------------

.. important::

   The backup of HSS ransomware protection depends on Cloud Backup and Recovery (CBR). Before enabling server backup, ensure that you have applied for CBR.

#. Log in to the management console and go to the HSS page.

#. In the navigation pane, choose **Prevention** > **Ransomware Prevention**. The protected server list is displayed. Click the policy name in the **Backup Policy Status** column of the target server.

#. Configure the policy in the dialog box that is displayed. For more information, see :ref:`Table 4 <hss_01_0347__table1463142913399>`.

   .. _hss_01_0347__table1463142913399:

   .. table:: **Table 4** Policy parameters

      +-----------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
      | Parameter             | Description                                                                                                                                                                                                                              | Example Value         |
      +=======================+==========================================================================================================================================================================================================================================+=======================+
      | Backup Frequency      | Data can be automatically backed up on specific days in a week, or at a fixed interval.                                                                                                                                                  | Weekly                |
      |                       |                                                                                                                                                                                                                                          |                       |
      |                       | -  **Weekly**: Select one or more days in a week to back up data.                                                                                                                                                                        |                       |
      |                       | -  **Day based**: The range of the backup interval is 1 to 30 days.                                                                                                                                                                      |                       |
      +-----------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
      | Execution Time        | Time when automated backup is started.                                                                                                                                                                                                   | 00:00, 07:00          |
      |                       |                                                                                                                                                                                                                                          |                       |
      |                       | .. note::                                                                                                                                                                                                                                |                       |
      |                       |                                                                                                                                                                                                                                          |                       |
      |                       |    Example of policy configurations                                                                                                                                                                                                      |                       |
      |                       |                                                                                                                                                                                                                                          |                       |
      |                       |    Policy 1: Set **Backup Frequency** to **Weekly**, select **Wednesday** and **Saturday**, and set **Execution Time** to **00:00** and **13:00**. Data will be automatically backed up at 00:00 and 13:00 every Wednesday and Saturday. |                       |
      |                       |                                                                                                                                                                                                                                          |                       |
      |                       |    Policy 2: Set **Backup Frequency** to **Day based** and set the interval to two days. Set **Execution Time** to **02:00** and **14:00**. Data will be automatically backed up at 02:00 and 14:00 at an interval of two days.          |                       |
      +-----------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
      | Timezone              | Select the time zone of the backup time.                                                                                                                                                                                                 | UTC+08:00             |
      +-----------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+

#. Confirm the settings and click **Next**. Configure the backup retention rule.

   -  **Type**: **Backup Quantity**

      Configure the backup policy. For more information, see :ref:`Table 5 <hss_01_0347__table238419613134>`.

      .. _hss_01_0347__table238419613134:

      .. table:: **Table 5** Parameters for data retention by quantity

         +-----------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------+
         | Parameter                   | Description                                                                                                                                                                                                             | Example Value                                                  |
         +=============================+=========================================================================================================================================================================================================================+================================================================+
         | Rule                        | Number of latest backups to be retained.                                                                                                                                                                                | 30                                                             |
         |                             |                                                                                                                                                                                                                         |                                                                |
         |                             | .. important::                                                                                                                                                                                                          |                                                                |
         |                             |                                                                                                                                                                                                                         |                                                                |
         |                             |    NOTICE:                                                                                                                                                                                                              |                                                                |
         |                             |    This setting takes effect no matter how you configure advanced options.                                                                                                                                              |                                                                |
         |                             |                                                                                                                                                                                                                         |                                                                |
         |                             |    For example, if the rule is configured to keep the most recent 30 backups, and **Advanced Options** are configured to keep the latest backup in the last 3 months (90 days), the latest 30 backups will be retained. |                                                                |
         +-----------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------+
         | (Optional) Advanced Options | Daily backup: The latest backup on each of the specified days is retained.                                                                                                                                              | Keep the most recent backup from each of the last three months |
         +-----------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------+

   -  **Type**: **Time period**

      Configure the backup policy. For more information, see :ref:`Table 6 <hss_01_0347__table057910431715>`.

      .. _hss_01_0347__table057910431715:

      .. table:: **Table 6** Parameters for data retention by time period

         +-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
         | Parameter             | Description                                                                                                                                                          | Example Value         |
         +=======================+======================================================================================================================================================================+=======================+
         | Rule                  | Select or customize a backup retention period. The system will automatically retain backups and delete old ones based on your settings. The retention period can be: | 3 months              |
         |                       |                                                                                                                                                                      |                       |
         |                       | -  Days                                                                                                                                                              |                       |
         |                       | -  1 month                                                                                                                                                           |                       |
         |                       | -  3 months                                                                                                                                                          |                       |
         |                       | -  6 months                                                                                                                                                          |                       |
         |                       | -  1 year                                                                                                                                                            |                       |
         +-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+

   -  **Type**: **Permanent**

      Backup data will be permanently stored.

      .. note::

         If the **Retention Type** of a rule is changed from **Time period** to Permanent, historical backups will still be deleted by following based on the **Time period** settings.

#. Click **OK**.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

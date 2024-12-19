:original_name: hss_01_0492.html

.. _hss_01_0492:

Managing Server Backup
======================

After ransomware backup is enabled, the backup vault periodically backs up your servers based on the backup policy. You can expand the vault capacity or modify the backup policy as required.

Prerequisites
-------------

Ransomware backup has been enabled. For details, see :ref:`Enabling Backup <hss_01_0562>`.

Increasing the Backup Capacity
------------------------------

#. Log in to the management console and go to the HSS page.

#. In the navigation pane, choose **Prevention** > **Ransomware Prevention**. The protected server list is displayed. Click **Add Capacity** in the **Operation** column of the target server.

#. In the displayed dialog box, configure the capacity.

#. If the information is correct, click **OK**. The payment page is displayed. After the payment is complete, return to the **Protected Server** tab page to view the storage capacity of the target server.

   If the payment is not complete, the **Vault Status** of the target server is **Locked**. After the payment, the status becomes normal.

Modifying a Backup Policy
-------------------------

#. Log in to the management console and go to the HSS page.

#. In the navigation pane, choose **Prevention** > **Ransomware Prevention**. The protected server list is displayed. Click the policy name in the **Backup Policy Status** column of the target server.

#. In the displayed dialog box, configure the policy. For details about the parameters, see :ref:`Policy parameters <hss_01_0492__table1463142913399>`.

   .. _hss_01_0492__table1463142913399:

   .. table:: **Table 1** Policy parameters

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

   -  **Type**: **Backup quantity**

      :ref:`Table 2 <hss_01_0492__table238419613134>` describes the parameters for configuring a backup rule.

      .. _hss_01_0492__table238419613134:

      .. table:: **Table 2** Parameters for data retention by quantity

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
         | (Optional) Advanced Options | You can retain the latest backup in a day, a week, a month, or a year.                                                                                                                                                  | Keep the most recent backup from each of the last three months |
         +-----------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------+

   -  **Type**: **Time period**

      :ref:`Table 3 <hss_01_0492__table057910431715>` describes the parameters for configuring a backup rule.

      .. _hss_01_0492__table057910431715:

      .. table:: **Table 3** Parameters for data retention by time period

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

         If the **Retention Type** of a rule is changed from **Time period** to another, historical backups will still be deleted based on the **Time period** settings.

#. Click **OK**.

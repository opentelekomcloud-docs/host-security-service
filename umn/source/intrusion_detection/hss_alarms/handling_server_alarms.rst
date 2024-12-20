:original_name: hss_01_0413.html

.. _hss_01_0413:

Handling Server Alarms
======================

The **Events** page displays the alarms generated in the last 30 days.

The status of a handled alarm changes from **Unhandled** to **Handled**.

Limitations and Constraints
---------------------------

-  To skip the checks on high-risk command execution, privilege escalations, reverse shells, abnormal shells, or web shells, manually disable the corresponding policies in the policy groups on the **Policies** page. HSS will not check the servers associated with disabled policies.
-  Other detection items cannot be manually disabled.
-  Servers that are not protected by HSS do not support operations related to alarms and events.


Handling Server Alarms
----------------------

This section describes how you should handle alarms to enhance server security.

.. note::

   Do not fully rely on alarm handling to defend against attacks, because not every issue can be detected in a timely manner. You are advised to take more measures to prevent threats, such as checking for and fixing vulnerabilities and unsafe settings.

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane on the left, choose **Intrusion Detection** > **Alarms** and click **Server Alarms**.


   .. figure:: /_static/images/en-us_image_0000001621827002.png
      :alt: **Figure 1** Server alarms

      **Figure 1** Server alarms

#. Click an alarm name to view the alarm details and suggestions.

#. Handle alarms.

   .. note::

      Alarms are displayed on the **Server Alarms** page. Here you can check up to 30 days of historical alarms.

      Check and handle alarms as needed. The status of a handled alarm changes from **Unhandled** to **Handled**.

   -  Handling a single alarm

      In the **Operation** column of an alarm, click **Handle**.

   -  Handling alarms in batches

      Select all alarms and click **Batch Handle** above the alarm list.

   -  Handling all alarms

      In the **Alarms to be Handled** area on the left pane of the alarm list, select an alarm type and click **Handle All** above the alarm list.

#. In the **Handle Event** dialog box, select an action. For details about the alarm handling actions, see :ref:`Table 1 <hss_01_0413__table023915918117>`.

   .. _hss_01_0413__table023915918117:

   .. table:: **Table 1** Alarm handling methods

      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Action                            | Description                                                                                                                                                                                                                                                         |
      +===================================+=====================================================================================================================================================================================================================================================================+
      | Ignore                            | Ignore the current alarm. Any new alarms of the same type will still be reported by HSS.                                                                                                                                                                            |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Isolate and kill                  | If a program is isolated and killed, it will be terminated immediately and no longer able to perform read or write operations. Isolated source files of programs or processes are displayed on the **Isolated Files** slide-out panel and cannot harm your servers. |
      |                                   |                                                                                                                                                                                                                                                                     |
      |                                   | You can click **Isolated Files** on the upper right corner to check the files. For details, see :ref:`Managing Isolated Files <hss_01_0331>`.                                                                                                                       |
      |                                   |                                                                                                                                                                                                                                                                     |
      |                                   | For details about events that can be isolated and killed, see :ref:`Server Alarms <hss_01_0277>`.                                                                                                                                                                   |
      |                                   |                                                                                                                                                                                                                                                                     |
      |                                   | .. note::                                                                                                                                                                                                                                                           |
      |                                   |                                                                                                                                                                                                                                                                     |
      |                                   |    When a program is isolated and killed, the process of the program is terminated immediately. To avoid impact on services, check the detection result, and cancel the isolation of or unignore misreported malicious programs (if any).                           |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Mark as handled                   | Mark the event as handled. You can add remarks for the event to record more details.                                                                                                                                                                                |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Add to process whitelist          | If you can confirm that a process triggering an alarm can be trusted, you can add it to the process whitelist. HSS will no longer report alarms on whitelisted processes.                                                                                           |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Add to Login Whitelist            | Add false alarmed items of the **Brute-force attack** and **Abnormal login** types to the Login Whitelist.                                                                                                                                                          |
      |                                   |                                                                                                                                                                                                                                                                     |
      |                                   | HSS will no longer report alarm on the Login Whitelist. A whitelisted login event will not trigger alarms.                                                                                                                                                          |
      |                                   |                                                                                                                                                                                                                                                                     |
      |                                   | The following alarm events can be added:                                                                                                                                                                                                                            |
      |                                   |                                                                                                                                                                                                                                                                     |
      |                                   | -  Brute-force attacks                                                                                                                                                                                                                                              |
      |                                   | -  Abnormal logins                                                                                                                                                                                                                                                  |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Add to alarm whitelist            | Add false alarmed items to the login whitelist.                                                                                                                                                                                                                     |
      |                                   |                                                                                                                                                                                                                                                                     |
      |                                   | HSS will no longer report alarm on the whitelisted items. A whitelisted alarm will not trigger alarms.                                                                                                                                                              |
      |                                   |                                                                                                                                                                                                                                                                     |
      |                                   | For details about events that can be isolated and killed, see :ref:`Server Alarms <hss_01_0277>`.                                                                                                                                                                   |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Click **OK**.

   You check handled alarms. For details, see :ref:`Handling History <hss_01_0508>`.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

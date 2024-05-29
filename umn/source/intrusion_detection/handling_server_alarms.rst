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

Procedure
---------

This section describes how you should handle alarms to enhance server security.

.. note::

   Do not fully rely on alarm handling to defend against attacks, because not every issue can be detected in a timely manner. You are advised to take more measures to prevent threats, such as checking for and fixing vulnerabilities and unsafe settings.

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

#. In the navigation pane on the left, choose **Detection** > **Alarms** and click **Server Alarms**.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.


   .. figure:: /_static/images/en-us_image_0000001621827002.png
      :alt: **Figure 1** Server alarms

      **Figure 1** Server alarms

   .. table:: **Table 1** Alarm statistics

      +-----------------------+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter             |                       | Description                                                                                                                                                                                                                                                                      |
      +=======================+=======================+==================================================================================================================================================================================================================================================================================+
      | Enterprise Project    |                       | Select an enterprise project and view alarm details by enterprise project.                                                                                                                                                                                                       |
      +-----------------------+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Time range            |                       | You can select a fixed time period or customize a time period to filter alarms. Only alarms generated within 30 days can be queried.                                                                                                                                             |
      |                       |                       |                                                                                                                                                                                                                                                                                  |
      |                       |                       | The options are as follows:                                                                                                                                                                                                                                                      |
      |                       |                       |                                                                                                                                                                                                                                                                                  |
      |                       |                       | -  Last 24 hours                                                                                                                                                                                                                                                                 |
      |                       |                       | -  Last 3 days                                                                                                                                                                                                                                                                   |
      |                       |                       | -  Last 7 days                                                                                                                                                                                                                                                                   |
      |                       |                       | -  Last 30 days                                                                                                                                                                                                                                                                  |
      |                       |                       | -  Custom                                                                                                                                                                                                                                                                        |
      +-----------------------+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Server Alarms         | Affected Servers      | Number of servers for which alarms are generated.                                                                                                                                                                                                                                |
      +-----------------------+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      |                       | Alarms to be Handled  | Number of alarms to be handled.                                                                                                                                                                                                                                                  |
      |                       |                       |                                                                                                                                                                                                                                                                                  |
      |                       |                       | By default, all alarms to be handled are displayed.                                                                                                                                                                                                                              |
      +-----------------------+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      |                       | Handled Alarms        | Number of handled alarms.                                                                                                                                                                                                                                                        |
      +-----------------------+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      |                       | Blocked IP Addresses  | Number of blocked IP addresses. You can click the number to check blocked IP address list.                                                                                                                                                                                       |
      |                       |                       |                                                                                                                                                                                                                                                                                  |
      |                       |                       | The blocked IP address list displays the server name, attack source IP address, login type, blocking status, number of blocks, blocking start time, and the latest blocking time.                                                                                                |
      |                       |                       |                                                                                                                                                                                                                                                                                  |
      |                       |                       | If a valid IP address is blocked by mistake (for example, after O&M personnel enter incorrect passwords for multiple times), you can manually unblock it. If a server is frequently attacked, you are advised to fix its vulnerabilities in a timely manner and eliminate risks. |
      |                       |                       |                                                                                                                                                                                                                                                                                  |
      |                       |                       | .. important::                                                                                                                                                                                                                                                                   |
      |                       |                       |                                                                                                                                                                                                                                                                                  |
      |                       |                       |    NOTICE:                                                                                                                                                                                                                                                                       |
      |                       |                       |                                                                                                                                                                                                                                                                                  |
      |                       |                       |    -  After a blocked IP address is unblocked, HSS will no longer block the operations performed by the IP address.                                                                                                                                                              |
      |                       |                       |                                                                                                                                                                                                                                                                                  |
      |                       |                       |    -  A maximum of 10,000 IP addresses can be blocked for each type of software.                                                                                                                                                                                                 |
      |                       |                       |                                                                                                                                                                                                                                                                                  |
      |                       |                       |       If your Linux server does not support ipset, a maximum of 50 IP addresses can be clocked for MySQL and vsftp.                                                                                                                                                              |
      |                       |                       |                                                                                                                                                                                                                                                                                  |
      |                       |                       |       If your Linux server does not support ipset or hosts.deny, a maximum of 50 IP addresses can be blocked for SSH.                                                                                                                                                            |
      +-----------------------+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      |                       | Isolated Files        | HSS can isolate detected threat files. Files that have been isolated are displayed on a slide-out panel on the **Server Alarms** page. You can click **Isolated Files** on the upper right corner to check them.                                                                 |
      |                       |                       |                                                                                                                                                                                                                                                                                  |
      |                       |                       | You can recover isolated files. For details, see :ref:`Managing Isolated Files <hss_01_0331>`.                                                                                                                                                                                   |
      +-----------------------+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Container Alarms      | Affected Servers      | Number of servers for which alarms are generated.                                                                                                                                                                                                                                |
      +-----------------------+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      |                       | Alarms to be Handled  | Number of alarms to be handled.                                                                                                                                                                                                                                                  |
      |                       |                       |                                                                                                                                                                                                                                                                                  |
      |                       |                       | By default, all alarms to be handled are displayed.                                                                                                                                                                                                                              |
      +-----------------------+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      |                       | Handled Alarms        | Number of handled alarms                                                                                                                                                                                                                                                         |
      +-----------------------+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      |                       | Threats               | Displays the statistics on alarms by severity.                                                                                                                                                                                                                                   |
      |                       |                       |                                                                                                                                                                                                                                                                                  |
      |                       |                       | -  Critical                                                                                                                                                                                                                                                                      |
      |                       |                       | -  High                                                                                                                                                                                                                                                                          |
      |                       |                       | -  Medium                                                                                                                                                                                                                                                                        |
      |                       |                       | -  Low                                                                                                                                                                                                                                                                           |
      +-----------------------+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      |                       | Top 5 Events          | Displays the top 5 alarm types and their quantities.                                                                                                                                                                                                                             |
      +-----------------------+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Handle alarms.

   .. note::

      Alarms are displayed on the **Server Alarms** page. Here you can check up to 30 days of historical alarms.

      Check and handle alarms as needed. The status of a handled alarm changes from **Unhandled** to **Handled**. HSS will no longer collect its statistics or display them on the **Dashboard** page.

   -  Handling all alarms

      a. Select all of the alarms and click **Handle All**.

         .. note::

            Ensure that you have selected the minimum alarm event type. Otherwise, the **Handle All** button is unavailable.

      b. In the dialog box that is displayed, select a handling method, confirm the information, and click **OK**. For more information, see :ref:`Table 2 <hss_01_0413__table12568105515583>`.

         .. note::

            An alarm in the **Handled** state cannot be batch handled.

   -  Handling alarms in batches

      a. Select an event type, select multiple alarms, and click **Batch Handle**.
      b. In the dialog box that is displayed, select a handling method, confirm the information, and click **OK**. For more information, see :ref:`Table 2 <hss_01_0413__table12568105515583>`.

   -  Handling a single alarm

      a. Select an event type and click **Handle** in the **Operation** column of an alarm.
      b. In the dialog box that is displayed, select a handling method, confirm the information, and click **OK**. For more information, see :ref:`Table 2 <hss_01_0413__table12568105515583>`.

   .. _hss_01_0413__table12568105515583:

   .. table:: **Table 2** Alarm handling methods

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
      | Add to Login Whitelist            | Add false alarmed items of the **Brute-force attack** and **Abnormal login** types to the Login Whitelist.                                                                                                                                                          |
      |                                   |                                                                                                                                                                                                                                                                     |
      |                                   | HSS will no longer report alarm on the Login Whitelist. A whitelisted login event will not trigger alarms.                                                                                                                                                          |
      |                                   |                                                                                                                                                                                                                                                                     |
      |                                   | The following alarm events can be added to the Login Whitelist:                                                                                                                                                                                                     |
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

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

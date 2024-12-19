:original_name: hss_01_0414.html

.. _hss_01_0414:

Handling Container Alarms
=========================

HSS displays alarm and event statistics and their summary all on one page. You can have a quick overview of alarms, including the numbers of containers with alarms, handled alarms, and unhandled alarms.

The **Events** page displays the alarms generated in the last 30 days.

The status of a handled alarm changes from **Unhandled** to **Handled**.

Constraints
-----------

Servers that are not protected by HSS do not support operations related to alarms and events.


Handling Container Alarms
-------------------------

This section describes how you should handle alarms to enhance server security.

.. note::

   Do not fully rely on alarm handling to defend against attacks, because not every issue can be detected in a timely manner. You are advised to take more measures to prevent threats, such as checking for and fixing vulnerabilities and unsafe settings.

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane on the left, choose **Intrusion Detection** > **Alarms**, and click **Container Alarms**.


   .. figure:: /_static/images/en-us_image_0000001670234665.png
      :alt: **Figure 1** Container alarms

      **Figure 1** Container alarms

#. Click an alarm name to view the alarm details and suggestions.

#. Handle alarms.

   .. note::

      Alarms are displayed on the **Container Alarms** page. Here you can check up to 30 days of historical alarms.

      Check and handle alarms as needed. The status of a handled alarm changes from **Unhandled** to **Handled**. HSS will no longer collect its statistics.

   -  Handling a single alarm

      In the **Operation** column of an alarm, click **Handle**.

   -  Handling alarms in batches

      Select all alarms and click **Batch Handle** above the alarm list.

   -  Handling all alarms

      In the **Alarms to be Handled** area on the left pane of the alarm list, select an alarm type and click **Handle All** above the alarm list.

#. In the **Handle Event** dialog box, select an action. For details about the processing modes, see :ref:`Table 1 <hss_01_0414__table023915918117>`.

   .. _hss_01_0414__table023915918117:

   .. table:: **Table 1** Alarm handling methods

      +-----------------------------------+----------------------------------------------------------------------------------------------------------------+
      | Action                            | Description                                                                                                    |
      +===================================+================================================================================================================+
      | Ignore                            | Ignore the current alarm. Any new alarms of the same type will still be reported by HSS.                       |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------+
      | Mark as handled                   | Mark the event as handled. You can add remarks for the event to record more details.                           |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------+
      | Add to Login Whitelist            | Add false alarmed items of the **Brute-force attack** and **Abnormal login** types to the Login Whitelist.     |
      |                                   |                                                                                                                |
      |                                   | HSS will no longer report alarm on the Login Whitelist. A whitelisted login event will not trigger alarms.     |
      |                                   |                                                                                                                |
      |                                   | The following alarm events can be added:                                                                       |
      |                                   |                                                                                                                |
      |                                   | -  Brute-force attacks                                                                                         |
      |                                   | -  Abnormal logins                                                                                             |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------+
      | Add to process whitelist          | If you can confirm that a process triggering an alarm can be trusted, you can add it to the process whitelist. |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------+
      | Add to alarm whitelist            | Add false alarmed items to the login whitelist.                                                                |
      |                                   |                                                                                                                |
      |                                   | HSS will no longer report alarm on the whitelisted items. A whitelisted alarm will not trigger alarms.         |
      |                                   |                                                                                                                |
      |                                   | For details about events that can be isolated and killed, see :ref:`Container Alarm Events <hss_01_0312>`.     |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------+

#. Click **OK**.

   You check handled alarms. For details, see :ref:`Historical Records <hss_01_0508>`.

Canceling Handled Container Alarms
----------------------------------

You can cancel the processing of a handled alarm event.

#. In the alarm event list, filter handled alarms.
#. In the **Operation** column of an alarm, click **Handle**.
#. In the **Handle Alarm Event** dialog box, click **OK** to cancel the last handling.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

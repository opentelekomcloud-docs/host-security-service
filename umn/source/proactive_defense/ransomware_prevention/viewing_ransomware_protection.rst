:original_name: hss_01_0347.html

.. _hss_01_0347:

Viewing Ransomware Protection
=============================

After ransomware protection is enabled, if a ransomware attack event occurs on the server, the event will be recorded and displayed in the ransomware event list. You can handle the events based on your service requirements.

Constraints
-----------

After ransomware protection is enabled, you need to handle ransomware alarms and fix the vulnerabilities in your systems and middleware in a timely manner.

Viewing and Handling Ransomware Prevention Events
-------------------------------------------------

#. Log in to the management console.

#. Choose **Prevention** > **Ransomware Prevention**.

   .. note::

      If your servers are managed by enterprise projects, you can select the target enterprise project to view or operate the asset and detection information.

#. Click the **Events** tab and check events.

   To check alarm details, click an alarm name.

#. After confirming the severity of an event, click **Handle** in the **Operation** column of the target event to handle the event.

   You can also select multiple events and click **Batch Handle** above the list to handle events in batches.

#. In the **Handle Event** dialog box, select an action. For details, see :ref:`Table 1 <hss_01_0347__table1760114144115>`.

   .. _hss_01_0347__table1760114144115:

   .. table:: **Table 1** Alarm handling methods

      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                                                                                                                            |
      +===================================+========================================================================================================================================================================================================================================================================+
      | Action                            | -  Mark as handled                                                                                                                                                                                                                                                     |
      |                                   |                                                                                                                                                                                                                                                                        |
      |                                   |    For a manually handled event, you can add remarks to record the details about the event.                                                                                                                                                                            |
      |                                   |                                                                                                                                                                                                                                                                        |
      |                                   | -  Ignore                                                                                                                                                                                                                                                              |
      |                                   |                                                                                                                                                                                                                                                                        |
      |                                   |    Ignore the current alarm. Any new alarms of the same type will still be reported by HSS.                                                                                                                                                                            |
      |                                   |                                                                                                                                                                                                                                                                        |
      |                                   | -  Add to Alarm Whitelist                                                                                                                                                                                                                                              |
      |                                   |                                                                                                                                                                                                                                                                        |
      |                                   |    Add false alarmed items to the login whitelist.                                                                                                                                                                                                                     |
      |                                   |                                                                                                                                                                                                                                                                        |
      |                                   |    HSS will no longer report alarm on the whitelisted items. A whitelisted alarm will not trigger alarms.                                                                                                                                                              |
      |                                   |                                                                                                                                                                                                                                                                        |
      |                                   | -  Isolate and kill                                                                                                                                                                                                                                                    |
      |                                   |                                                                                                                                                                                                                                                                        |
      |                                   |    If a program is isolated and killed, it will be terminated immediately and no longer able to perform read or write operations. Isolated source files of programs or processes are displayed on the **Isolated Files** slide-out panel and cannot harm your servers. |
      |                                   |                                                                                                                                                                                                                                                                        |
      |                                   |    You can click **Isolated Files** on the upper right corner to check the files. For details, see :ref:`Managing Isolated Files <hss_01_0331>`.                                                                                                                       |
      |                                   |                                                                                                                                                                                                                                                                        |
      |                                   |    .. note::                                                                                                                                                                                                                                                           |
      |                                   |                                                                                                                                                                                                                                                                        |
      |                                   |       When a program is isolated and killed, the process of the program is terminated immediately. To avoid impact on services, check the detection result, and cancel the isolation of or unignore misreported malicious programs (if any).                           |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Batch Handle                      | If this option is selected, the same alarms triggered at different time are handled in batches. If no duplicate alarm is displayed after you select it, it indicates no duplicate alarms have been generated.                                                          |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Remarks                           | You can add remarks for convenient backtracking.                                                                                                                                                                                                                       |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

6. Click **OK**.

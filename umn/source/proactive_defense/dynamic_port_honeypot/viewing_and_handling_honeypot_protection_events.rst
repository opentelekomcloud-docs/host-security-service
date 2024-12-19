:original_name: hss_01_0601.html

.. _hss_01_0601:

Viewing and Handling Honeypot Protection Events
===============================================

Scenario
--------

By default, the servers that proactively connect to the dynamic honeypot port are compromised intranet servers. Once a suspicious connection behavior is detected, an alarm is reported.

This chapter describes how to view and handle these alarms and events.


Viewing and Handling Honeypot Protection Events
-----------------------------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. Choose **Prevention** > **Dynamic Port Honeypot**.

#. Under the introductions, view the protection overview.

   -  You can view the number of protection policies, protected servers, and protection events.
   -  You can enable the **Automatically apply default policies to newly add servers**. If is displayed, the function is enabled.

#. Click the **Protection Events** tab to view honeypot protection events. For details about the parameters in the event list, see :ref:`Table 1 <hss_01_0601__table0155155113423>`.

   .. _hss_01_0601__table0155155113423:

   .. table:: **Table 1** Parameters in the event list

      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                   |
      +===================================+===============================================================================================================================================================+
      | Alarm Name                        | The name of an alarm event. Click an alarm name to view the details. For details, see :ref:`Table 3 <hss_01_0601__table179173719273>`.                        |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Alert Severity                    | Alarm threat level. Honeypot protection events are classified into the following two levels:                                                                  |
      |                                   |                                                                                                                                                               |
      |                                   | -  High risk: The remote server connects to the honeypot port for multiple times.                                                                             |
      |                                   | -  Medium risk: The remote server is connected to the honeypot port.                                                                                          |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Alarm Summary                     | Summary of alarm events. Based on the information, you can learn about the server that may be compromised and the connection between the server and the port. |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Affected Asset                    | Dynamic port server connected to the compromised server.                                                                                                      |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Alarm Reported                    | Time when an alarm occurred.                                                                                                                                  |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Status                            | Alarm handling status, which can be **Handled** or **To be handled**.                                                                                         |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Operation                         | You can handle alarm events.                                                                                                                                  |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. After confirming the alarm information, click **Handle** in the **Operation** column of the event whose **Status** is **To be handled**. The **Handle Alarm** dialog box is displayed.

   If you need to handle multiple alarm events in batches, click **Batch Handle** in the upper left corner of the list.

#. Select a solution. For details about the solution, see :ref:`Table 2 <hss_01_0601__table1156710171708>`.

   .. _hss_01_0601__table1156710171708:

   .. table:: **Table 2** Parameters for handling alarm events

      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                 |
      +===================================+=============================================================================================================================================================+
      | Action                            | -  **Ignore**: Ignore the alarm event. The alarm is still generated when the next threat event occurs.                                                      |
      |                                   | -  **Mark as handled**: You can manually isolate ports for the compromised server.                                                                          |
      |                                   | -  **Add to alarm whitelist**: Add the trusted server that triggers an alarm to the whitelist so that no alarm will be generated when similar events occur. |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Batch Handle                      | If you need to handle the same alarm event at the same time, you can select the parameter.                                                                  |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | (Optional) Remarks                | To facilitate identification of the current processing, supplementary description can be provided.                                                          |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Click **OK**.

Alarm Details Parameters
------------------------

For details about the parameters on the alarm details, see :ref:`Table 3 <hss_01_0601__table179173719273>`.

.. _hss_01_0601__table179173719273:

.. table:: **Table 3** Alarm details parameters

   +---------------------+----------------------------------------------------------------------------------------------------------------------------------------+
   | Parameter           | Description                                                                                                                            |
   +=====================+========================================================================================================================================+
   | Intelligence Engine | Detection engines used by HSS, including the virus detection engine, AI detection engine, and malicious intelligence detection engine. |
   +---------------------+----------------------------------------------------------------------------------------------------------------------------------------+
   | Attack Status       | Status of the current threat.                                                                                                          |
   +---------------------+----------------------------------------------------------------------------------------------------------------------------------------+
   | First Occurred      | Time when an attack alarm is generated for the first time                                                                              |
   +---------------------+----------------------------------------------------------------------------------------------------------------------------------------+
   | Alarm ID            | Unique ID of an alarm                                                                                                                  |
   +---------------------+----------------------------------------------------------------------------------------------------------------------------------------+
   | ATT&CK Phase        | Attack model used by attackers in each phase.                                                                                          |
   +---------------------+----------------------------------------------------------------------------------------------------------------------------------------+
   | Last Occurred       | Time when an attack alarm was last generated                                                                                           |
   +---------------------+----------------------------------------------------------------------------------------------------------------------------------------+
   | Alarm Information   | Detailed information about an alarm, including the alarm description, alarm summary, affected assets, and handling suggestions.        |
   +---------------------+----------------------------------------------------------------------------------------------------------------------------------------+
   | Forensics           | The dynamic port honeypot function checks the network forensics information of the attack source.                                      |
   +---------------------+----------------------------------------------------------------------------------------------------------------------------------------+
   | Similar Alarms      | Alarms that are similar to the current alarm event. You can handle the alarm according to the handling method of the similar alarms.   |
   +---------------------+----------------------------------------------------------------------------------------------------------------------------------------+

Filtering Events in Different Handling Statuses
-----------------------------------------------

Select an event in the target status from the drop-down list.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

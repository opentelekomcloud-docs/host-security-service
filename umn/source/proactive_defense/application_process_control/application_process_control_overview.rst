:original_name: hss_01_0531.html

.. _hss_01_0531:

Application Process Control Overview
====================================

HSS can learn the characteristics of application processes on servers and manage their running. Suspicious and trusted processes are allowed to run, and alarms are generated for malicious processes.

Constraints and Limitations
---------------------------

-  Application process control is available only in HSS premium, WTP, and container editions.
-  To use application process control, ensure the agent installed on the server falls within the following range. For details about how to upgrade the agent, see :ref:`Upgrading the Agent <hss_01_0462>`.

   -  Linux: 3.2.7 or later
   -  Windows: 4.0.19 or later

Process of Using Application Process Control
--------------------------------------------


.. figure:: /_static/images/en-us_image_0000001666949664.png
   :alt: **Figure 1** Usage process

   **Figure 1** Usage process

.. table:: **Table 1** Process of using application process control

   +----------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Operation                                                            | Description                                                                                                                                                                                                                                                                                       |
   +======================================================================+===================================================================================================================================================================================================================================================================================================+
   | :ref:`Create a whitelist policy. <hss_01_0532>`                      | A whitelist policy specifies how HSS learns server behaviors and protect application processes. Application process protection can be enabled only for servers associated with a whitelist policy.                                                                                                |
   +----------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`Confirm learning outcomes. <hss_01_0533>`                      | After the HSS learns the application processes on servers, there may be some suspicious application processes with insignificant characteristics, and HSS cannot determine whether they are malicious or trustworthy. In this case, you need to confirm the learning outcomes.                    |
   +----------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`Enable application process control. <hss_01_0534>`             | Enable application process control on the servers associated with a policy.                                                                                                                                                                                                                       |
   +----------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`Check and handle suspicious processes. <hss_01_0535>`          | HSS cannot determine whether some suspicious application processes with insignificant characteristics are trustworthy. You need to check their process details, determine whether they are trustworthy, and add them to the process whitelist.                                                    |
   +----------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | (Optional) :ref:`Add items to the process whitelist. <hss_01_0563>`  | After HSS completes learning, if it regards many trustworthy application processes as suspicious, you can add these processes to the whitelist. HSS will extend the process whitelist after comparing the fingerprints of the processes it learned and those detected in asset fingerprint scans. |
   +----------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | (Optional) :ref:`Start learning on the servers again. <hss_01_0544>` | If you have added trustworthy processes to the whitelist but there are still many false positives reported, you can let HSS start learning again on the servers.                                                                                                                                  |
   +----------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

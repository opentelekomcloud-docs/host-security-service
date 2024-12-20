:original_name: hss_01_0650.html

.. _hss_01_0650:

Agent Overview
==============

What Is an Agent?
-----------------

The HSS agent is a piece of software installed on cloud servers to exchange data between the servers and HSS, implementing security detection and protection. If no agent is installed, the HSS is unavailable.

Scans all servers at 00:00 every day; monitors the security and monitors status of servers; and reports the collected server and monitors information (including non-compliant configurations, insecure configurations, intrusion traces, software list, port list, and process list) to the cloud protection center. In addition, the agent blocks attacks targeted at servers and containers based on the security policies you configured.

Supported OSs
-------------

Currently, some mainstream OSs are supported. For details, see :ref:`Supported OSs <hss_01_0647__section3897426874>`. To obtain better HSS service experience, you are advised to install or upgrade to an OS version supported by the agent.

Processes When the Agent Is Running
-----------------------------------

-  **Linux**

   The account of the agent is **root**. :ref:`Table 1 <hss_01_0650__hss_01_0386_table14932168797>` lists the running processes on a Linux server.

   .. _hss_01_0650__hss_01_0386_table14932168797:

   .. table:: **Table 1** Agent running process on a Linux server

      +--------------------+-----------------------------------------------------------------------+------------------------------------+
      | Agent Process Name | Function                                                              | Path                               |
      +====================+=======================================================================+====================================+
      | hostguard          | Detects security issues, protects the system, and monitors the agent. | /usr/local/hostguard/bin/hostguard |
      +--------------------+-----------------------------------------------------------------------+------------------------------------+
      | hostwatch          | Monitors the agent process.                                           | /usr/local/hostguard/bin/hostwatch |
      +--------------------+-----------------------------------------------------------------------+------------------------------------+
      | upgrade            | Upgrades the agent.                                                   | /usr/local/hostguard/bin/upgrade   |
      +--------------------+-----------------------------------------------------------------------+------------------------------------+

-  **Windows**

   The account of the agent is **system**. :ref:`Table 2 <hss_01_0650__hss_01_0386_table3329181017482>` lists the running processes on a Windows server.

   .. _hss_01_0650__hss_01_0386_table3329181017482:

   .. table:: **Table 2** Agent running process on a Windows server

      +--------------------+-----------------------------------------------------------------------+---------------------------------------------+
      | Agent Process Name | Function                                                              | Path                                        |
      +====================+=======================================================================+=============================================+
      | hostguard.exe      | Detects security issues, protects the system, and monitors the agent. | C:\\Program Files\\HostGuard\\HostGuard.exe |
      +--------------------+-----------------------------------------------------------------------+---------------------------------------------+
      | hostwatch.exe      | Monitors the agent process.                                           | C:\\Program Files\\HostGuard\\HostWatch.exe |
      +--------------------+-----------------------------------------------------------------------+---------------------------------------------+
      | upgrade.exe        | Upgrades the agent.                                                   | C:\\Program Files\\HostGuard\\upgrade.exe   |
      +--------------------+-----------------------------------------------------------------------+---------------------------------------------+

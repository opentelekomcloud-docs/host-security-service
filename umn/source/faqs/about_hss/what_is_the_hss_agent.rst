:original_name: hss_01_0245.html

.. _hss_01_0245:

What Is the HSS Agent?
======================

The HSS agent is used to scan all servers and containers, monitor their status in real time, and collect their information and report to the cloud protection center.

Functions of the Agent
----------------------

-  The agent runs scan tasks every day in the early morning to scan all servers and containers, monitors their security, and reports information collected from them to the cloud protection center.
-  The agent blocks attacks targeted at servers and containers based on the security policies you configured.

.. note::

   -  If no agent is installed or the agent installed is abnormal, the HSS is unavailable.

Linux Agent Processes
---------------------

The agent process needs to be run by the **root** user.

The agent contains the following processes:

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

Windows Agent Processes
-----------------------

The agent process needs to be run by the **system** user.

The agent contains the following processes:

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

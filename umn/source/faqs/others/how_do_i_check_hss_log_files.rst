:original_name: hss_01_0099.html

.. _hss_01_0099:

How Do I Check HSS Log Files?
=============================

Log Path
--------

The following table describes log files and their paths.

+-----------------------+-----------------------------------+--------------------------+
| OS                    | Log Directory                     | Log File                 |
+=======================+===================================+==========================+
| Linux                 | /var/log/hostguard/               | -  hostwatch.log         |
|                       |                                   | -  hostguard.log         |
|                       |                                   | -  upgrade.log           |
|                       |                                   | -  hostguard-service.log |
|                       |                                   | -  config_tool.log       |
|                       |                                   | -  engine.log            |
+-----------------------+-----------------------------------+--------------------------+
| Windows               | C:\\Program Files\\HostGuard\\log | -  hostwatch.log         |
|                       |                                   | -  hostguard.log         |
|                       |                                   | -  upgrade.log           |
+-----------------------+-----------------------------------+--------------------------+

Log Retention
-------------

+-----------------------+-----------------------------------------------------------------+--------------+--------------------+------------------------------------+
| Log File              | Description                                                     | Maximum Size | Retained File      | Retention Period                   |
+=======================+=================================================================+==============+====================+====================================+
| hostwatch.log         | Records logs generated during the running of daemon processes.  | 10MB         | Latest eight files | Until the HSS agent is uninstalled |
+-----------------------+-----------------------------------------------------------------+--------------+--------------------+------------------------------------+
| hostguard.log         | Records logs generated during the running of working processes. | 10MB         | Latest eight files |                                    |
+-----------------------+-----------------------------------------------------------------+--------------+--------------------+------------------------------------+
| upgrade.log           | Records logs generated during version upgrading.                | 10MB         | Latest eight files |                                    |
+-----------------------+-----------------------------------------------------------------+--------------+--------------------+------------------------------------+
| hostguard-service.log | Records logs (scripts) generated when the service starts.       | 100kB        | Latest two logs    |                                    |
+-----------------------+-----------------------------------------------------------------+--------------+--------------------+------------------------------------+
| config_tool.log       | Records logs (programs) generated when the service starts.      | 10kB         | Latest two logs    |                                    |
+-----------------------+-----------------------------------------------------------------+--------------+--------------------+------------------------------------+
| engine.log            | Records logs generated when the service exits.                  | 10kB         | Latest two logs    |                                    |
+-----------------------+-----------------------------------------------------------------+--------------+--------------------+------------------------------------+

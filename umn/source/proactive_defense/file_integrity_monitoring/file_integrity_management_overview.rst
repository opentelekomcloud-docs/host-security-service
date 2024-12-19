:original_name: hss_01_0359.html

.. _hss_01_0359:

File Integrity Management Overview
==================================

File integrity management (FIM) monitors key files on Linux servers in real time; records file addition, modification, and deletion; and reports alarms, helping you detect suspicious changes in a timely manner.

File Integrity Monitoring Principles
------------------------------------

HSS checks for suspicious changes by comparing the previous and current statuses of a file.

File Integrity Monitoring Scope
-------------------------------

Some file monitoring paths are preconfigured in HSS. For details, see :ref:`Table 1 <hss_01_0359__table1653481217449>`.

To add or remove monitored files, you can modify parameters in the **File Integrity** area in the **File Protection** policy. For details, see :ref:`Configuring Policies <hss_01_0044>`.

.. _hss_01_0359__table1653481217449:

.. table:: **Table 1** Default file monitoring paths

   +-----------------------------------+-----------------------------------+
   | Type                              | File Path                         |
   +===================================+===================================+
   | bin                               | -  /bin/ls                        |
   |                                   | -  /bin/ps                        |
   |                                   | -  /bin/bash                      |
   |                                   | -  /bin/login                     |
   +-----------------------------------+-----------------------------------+
   | usr                               | -  /usr/bin/ls                    |
   |                                   | -  /usr/bin/ps                    |
   |                                   | -  /usr/bin/bash                  |
   |                                   | -  /usr/bin/login                 |
   |                                   | -  /usr/bin/passwd                |
   |                                   | -  /usr/bin/top                   |
   |                                   | -  /usr/bin/killall               |
   |                                   | -  /usr/bin/ssh                   |
   |                                   | -  /usr/bin/wget                  |
   |                                   | -  /usr/bin/curl                  |
   +-----------------------------------+-----------------------------------+

Constraints and Limitations
---------------------------

File integrity management applies only to Linux servers.

:original_name: hss_01_0137.html

.. _hss_01_0137:

Constraints and Limitations
===========================

Supported Server Types
----------------------

Elastic Cloud Server (ECS)

.. _hss_01_0137__section3897426874:

Supported OSs
-------------

HSS can run on Linux servers (such as CentOS and EulerOS) and Windows servers (such as Windows 2012 and Windows 2016).

.. important::

   -  The agent is probably incompatible with the Linux or Windows versions that have reached end of life. To obtain better HSS service experience, you are advised to install or upgrade to an OS version supported by the agent.

-  Server OSs supported by the agent

   +-----------------------+-----------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | OS Type               | System Architecture   | Supported OS                                                                                                                                                                |
   +=======================+=======================+=============================================================================================================================================================================+
   | Linux                 | X86                   | -  CentOS 7.4, 7.5, 7.6, 7.7, 7.8, 7.9, 8.0, 8.1, 8.2, and 9 (64-bit)                                                                                                       |
   |                       |                       | -  Debian 9, 10, 11.0.0, 11.1.0 (64-bit)                                                                                                                                    |
   |                       |                       | -  EulerOS 2.2, 2.3, 2.5, 2.7 and 2.9 (64-bit)                                                                                                                              |
   |                       |                       | -  Fedora 28 (64-bit)                                                                                                                                                       |
   |                       |                       | -  OpenSUSE: 15.3 (64-bit)                                                                                                                                                  |
   |                       |                       | -  Ubuntu 16, 18, 20.03, 20.04, and 22.04 (64-bit)                                                                                                                          |
   |                       |                       | -  Red Hat 7.4, 7.6, 8.0, 8.7 (64-bit)                                                                                                                                      |
   |                       |                       | -  OpenEuler 20.03 LTS, 22.03 SP3 LTS, and 22.03 (64-bit)                                                                                                                   |
   |                       |                       | -  AlmaLinux 9.0 (64-bit)                                                                                                                                                   |
   |                       |                       | -  Rocky Linux 8.4, 8.5 and 9.0 (64-bit)                                                                                                                                    |
   +-----------------------+-----------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   |                       | ARM                   | -  CentOS 7.4, 7.5, 7.6, 7.7, 7.8, 7.9, 8.0, 8.1, 8.2, and 9 (64-bit)                                                                                                       |
   |                       |                       | -  EulerOS 2.8 and 2.9 (64-bit)                                                                                                                                             |
   |                       |                       | -  Fedora 29 (64-bit)                                                                                                                                                       |
   |                       |                       | -  OpenSUSE: 15 64bit with ARM(40GB)                                                                                                                                        |
   |                       |                       | -  Ubuntu 18 (64-bit)                                                                                                                                                       |
   |                       |                       | -  Kylin V7 and V10 (64-bit)                                                                                                                                                |
   |                       |                       | -  NeoKylin: V10 (aarch64-bit)                                                                                                                                              |
   +-----------------------+-----------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Windows               | X86                   | -  Windows Server 2019                                                                                                                                                      |
   |                       |                       | -  Windows Server 2016                                                                                                                                                      |
   |                       |                       | -  Windows Server 2012                                                                                                                                                      |
   |                       |                       | -  Windows Server 2008                                                                                                                                                      |
   |                       |                       |                                                                                                                                                                             |
   |                       |                       |    .. note::                                                                                                                                                                |
   |                       |                       |                                                                                                                                                                             |
   |                       |                       |       If any third-party security software is installed on the server, disable the protection function of the software before agent installation, and enable it afterwards. |
   +-----------------------+-----------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

OSs that Support Vulnerability Scan and Fix
-------------------------------------------

HSS can scan for and fix vulnerabilities in the OSs described in :ref:`Table 1 <hss_01_0137__table1796232221619>`.

.. _hss_01_0137__table1796232221619:

.. table:: **Table 1** OSs that support vulnerability scan and fix

   +-----------------------------------+-------------------------------------------------------------+
   | OS Type                           | Supported OS                                                |
   +===================================+=============================================================+
   | Windows                           | -  Windows Server 2019 Datacenter 64-bit English (40 GB)    |
   |                                   | -  Windows Server 2019 Datacenter 64-bit Chinese (40 GB)    |
   |                                   | -  Windows Server 2016 Standard 64-bit English (40 GB)      |
   |                                   | -  Windows Server 2016 Standard 64-bit Chinese (40 GB)      |
   |                                   | -  Windows Server 2016 Datacenter 64-bit English (40 GB)    |
   |                                   | -  Windows Server 2016 Datacenter 64-bit Chinese (40 GB)    |
   |                                   | -  Windows Server 2012 R2 Standard 64-bit English (40 GB)   |
   |                                   | -  Windows Server 2012 R2 Standard 64-bit Chinese (40 GB)   |
   |                                   | -  Windows Server 2012 R2 Datacenter 64-bit English (40 GB) |
   |                                   | -  Windows Server 2012 R2 Datacenter 64-bit Chinese (40 GB) |
   +-----------------------------------+-------------------------------------------------------------+
   | Linux                             | -  EulerOS: 2.2, 2.3, 2.5, 2.8, 2.9 (64-bit)                |
   |                                   | -  CentOS 7.4, 7.5, 7.6, 7.7, 7.8 and 7.9 (64-bit)          |
   |                                   | -  Ubuntu 16.04, 18.04, 20.04 (64-bit)                      |
   |                                   | -  Debian 9 and 10 (64-bit)                                 |
   |                                   | -  Kylin V10 (64-bit)                                       |
   |                                   | -  UnionTech OS V20 server E and V20 server D (64-bit)      |
   +-----------------------------------+-------------------------------------------------------------+

:original_name: hss_01_0017.html

.. _hss_01_0017:

What Are the Differences Between the Web Tamper Protection Functions of HSS and WAF?
====================================================================================

The web tamper protection function of HSS monitors website directories in real time, backs up files, and restores tampered files using the backup, protecting websites from tampering. This function is helpful for governments, educational institutions, and enterprises.

WAF protects user data on the application layer. It supports cache configuration on static web pages. When a user accesses a web page, the system returns a cached page to the user and randomly checks whether the page has been tampered with.

Differences Between the Web Tamper Protection Functions of HSS and WAF
----------------------------------------------------------------------

The following table describes the differences between HSS and WAF.

.. table:: **Table 1** Differences between the web tamper protection functions of HSS and WAF

   +-----------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------+
   | Item                        | HSS                                                                                                                                                    | WAF                                                     |
   +=============================+========================================================================================================================================================+=========================================================+
   | Static web page protection  | -  Drive file and web file locking                                                                                                                     | -  Static web pages can be cached on servers.           |
   |                             |                                                                                                                                                        | -  Privileged process management is not supported.      |
   |                             |    Locks files in driver and web file directories to prevent attackers from tampering with them.                                                       |                                                         |
   |                             |                                                                                                                                                        |                                                         |
   |                             | -  Privileged process management                                                                                                                       |                                                         |
   |                             |                                                                                                                                                        |                                                         |
   |                             |    Allows privileged processes to modify web pages.                                                                                                    |                                                         |
   +-----------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------+
   | Dynamic web page protection | Protects your data while Tomcat is running, detecting dynamic data tampering in databases.                                                             | No                                                      |
   +-----------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------+
   | Backup and restoration      | -  Active backup and restoration                                                                                                                       | No                                                      |
   |                             |                                                                                                                                                        |                                                         |
   |                             |    If WTP detects that a file in the protection directory is tampered with, it immediately uses the backup file on the local host to restore the file. |                                                         |
   |                             |                                                                                                                                                        |                                                         |
   |                             | -  Remote backup and restoration                                                                                                                       |                                                         |
   |                             |                                                                                                                                                        |                                                         |
   |                             |    If a file directory or backup directory on the local server is invalid, you can use the remote backup service to restore the tampered web page.     |                                                         |
   +-----------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------+
   | Suitable for                | Websites that have high security requirements and difficult to be manually recovered                                                                   | Websites that only require application-layer protection |
   +-----------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------+

How Do I Select WTP?
--------------------

+-------------------------------------------------------------------------+----------------------------------------------------+
| Website                                                                 | Service                                            |
+=========================================================================+====================================================+
| Common websites                                                         | WAF web tamper protection + HSS enterprise edition |
+-------------------------------------------------------------------------+----------------------------------------------------+
| Websites that require strong protection and anti-tampering capabilities | WAF web tamper protection + HSS WTP                |
+-------------------------------------------------------------------------+----------------------------------------------------+

:original_name: hss_01_0021.html

.. _hss_01_0021:

WTP Edition
===========

The WTP edition provides web tamper protection capabilities for your servers.

Web Tamper Protection Principles
--------------------------------

.. table:: **Table 1** How WTP works

   +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Type                              | Mechanism                                                                                                                                                                                           |
   +===================================+=====================================================================================================================================================================================================+
   | Static web page protection        | #. Local directory lock                                                                                                                                                                             |
   |                                   |                                                                                                                                                                                                     |
   |                                   |    WTP locks files in a web file directory in a drive to prevent attackers from modifying them. Website administrators can update the website content by using privileged processes.                |
   |                                   |                                                                                                                                                                                                     |
   |                                   | #. Proactive backup and restoration                                                                                                                                                                 |
   |                                   |                                                                                                                                                                                                     |
   |                                   |    If WTP detects that a file in the protection directory is tampered with, it immediately uses the backup file on the local host to restore the file.                                              |
   |                                   |                                                                                                                                                                                                     |
   |                                   | #. Remote backup and restoration                                                                                                                                                                    |
   |                                   |                                                                                                                                                                                                     |
   |                                   |    If a file directory or backup directory on the local server is invalid, you can use the remote backup service to restore the tampered web page.                                                  |
   +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Dynamic web page protection       | Dynamic web page protection for Tomcat.                                                                                                                                                             |
   |                                   |                                                                                                                                                                                                     |
   |                                   | #. Malicious behavior filtering based on RASP                                                                                                                                                       |
   |                                   |                                                                                                                                                                                                     |
   |                                   |    The unique runtime application self-protection (RASP) detects application program behaviors, preventing attackers from tampering with web pages through application programs.                    |
   |                                   |                                                                                                                                                                                                     |
   |                                   | #. Network disk file access control                                                                                                                                                                 |
   |                                   |                                                                                                                                                                                                     |
   |                                   |    WTP implements fine-grained management to control permissions for adding, modifying, and querying file content in network disks, preventing tampering without affecting website content release. |
   +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Prerequisite
------------

-  The agent has been installed on the servers to be protected, the agent status is **Online**, and the protection status is **Unprotected**.

Configuring Protected Directories
---------------------------------

You can add up to 50 directories to be protected. For details, see :ref:`Adding a Protected Directory <hss_01_0216__section4367121594314>`.

To record the running status of the server in real time, exclude the log files in the protected directory. You can grant high read and write permissions for log files to prevent attackers from viewing or tampering with the log files.

Procedure
---------

#. Log in to the management console.
#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

3. In the navigation pane, choose **Protection** > **Web Tamper Protection**. On the **Web Tamper Protection** page, click the **Servers** tab.


   .. figure:: /_static/images/en-us_image_0000001854854673.png
      :alt: **Figure 1** Entering the page for protected directory settings

      **Figure 1** Entering the page for protected directory settings

4. Click **Add Server**. In the displayed dialog box, select servers.

   .. note::

      Selected servers must be equal to or fewer than the available quotas.


   .. figure:: /_static/images/en-us_image_0000001563800218.png
      :alt: **Figure 2** Adding protected servers

      **Figure 2** Adding protected servers

5. Click **Add and Enable Protection** and check the protection status. Choose **Protection** > **Web Tamper Protection**. On the **Web Tamper Protection** page, click the **Servers** tab. If the **Protection Status** of the server is **Protected**, WTP has been enabled.

   .. important::

      -  After WTP is enabled, configure protected directories for WTP to take effect. For details, see :ref:`Adding a Protected Directory <hss_01_0216>`.

      -  Dynamic WTP can only be enabled for Linux servers, and can only be used after Tomcat is restarted.

      -  You can check the server protection status on the **Web Tamper Protection** page.

         The premium edition will be enabled when you enable WTP. You can perform the following operations to check the protection status:

         -  Choose **Prevention** > **Web Tamper Protection**. If the **Protection Status** of the server is **Protected**, WTP has been enabled.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

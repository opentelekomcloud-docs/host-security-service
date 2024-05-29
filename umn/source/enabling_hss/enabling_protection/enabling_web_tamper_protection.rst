:original_name: hss_01_0214.html

.. _hss_01_0214:

Enabling Web Tamper Protection
==============================

Before enabling WTP, you need to allocate a quota to a specified server. If the service is disabled or the server is deleted, the quota can be allocated to other servers.

The premium edition will be enabled when you enable WTP.

How WTP Prevents Web Page Tampering
-----------------------------------

.. table:: **Table 1** Protection mechanisms

   +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Type                              | Mechanism                                                                                                                                                                                           |
   +===================================+=====================================================================================================================================================================================================+
   | Static web page protection        | #. Local directory lock                                                                                                                                                                             |
   |                                   |                                                                                                                                                                                                     |
   |                                   |    WTP locks files in a web file directory in a drive to prevent attackers from modifying them. Website administrators can update the website content by using privileged processes.                |
   |                                   |                                                                                                                                                                                                     |
   |                                   | #. Active backup and restoration                                                                                                                                                                    |
   |                                   |                                                                                                                                                                                                     |
   |                                   |    If WTP detects that a file in the protection directory is tampered with, it immediately uses the backup file on the local host to restore the file.                                              |
   |                                   |                                                                                                                                                                                                     |
   |                                   | #. Remote backup and restoration                                                                                                                                                                    |
   |                                   |                                                                                                                                                                                                     |
   |                                   |    If a file directory or backup directory on the local server is invalid, you can use the remote backup service to restore the tampered web page.                                                  |
   +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Dynamic web page protection       | Provides runtime application self-protection (RASP) for Tomcat applications in the following ways:                                                                                                  |
   |                                   |                                                                                                                                                                                                     |
   |                                   | #. Malicious behavior filtering based on RASP                                                                                                                                                       |
   |                                   |                                                                                                                                                                                                     |
   |                                   |    The unique runtime application self-protection (RASP) detects application program behaviors, preventing attackers from tampering with web pages through application programs.                    |
   |                                   |                                                                                                                                                                                                     |
   |                                   | #. Network disk file access control                                                                                                                                                                 |
   |                                   |                                                                                                                                                                                                     |
   |                                   |    WTP implements fine-grained management to control permissions for adding, modifying, and querying file content in network disks, preventing tampering without affecting website content release. |
   +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Prerequisites
-------------

-  Choose **Prevention** > **Web Tamper Protection**. Click the **Servers** tab. The **Protection Status** of the server is **Unprotected**.
-  Choose **Asset Management** > **Servers & Quota**. The **Agent Status** of a server is **Online**, and the **Protection Status** of the server is **Unprotected**.

Setting Protected Directories
-----------------------------

You can set:

-  You can add a maximum of 50 protected directories to a host. For details, see "Adding a Protected Directory".
-  To record the running status of the server in real time, exclude the log files in the protected directory. You can grant high read and write permissions for log files to prevent attackers from viewing or tampering with the log files.

Enabling WTP
------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

#. In the navigation pane, choose **Prevention** > **Web Tamper Protection**. On the **Web Tamper Protection** page, click **Add Server**.


   .. figure:: /_static/images/en-us_image_0000001862372558.png
      :alt: **Figure 1** Adding protected servers

      **Figure 1** Adding protected servers

#. On the **Add Server** page, click the **Available servers** tab. Select the target server, select a quota from the drop-down list or retain the default value, and click **Add and Enable Protection**.

#. View the server status on the **Web Tamper Protection** page.

   The premium edition will be enabled when you enable WTP.

   -  Choose **Prevention** > **Web Tamper Protection**. If the **Protection Status** of the server is **Protected**, WTP has been enabled.
   -  Choose **Asset Management** > **Servers & Quota** and click the **Servers** tab. If the protection status of server is **Protected**, and **Disable** and **Switch Edition** are grayed out in the **Operation** column, the premium edition included with the WTP edition has been enabled.

.. important::

   -  A quota can be bound to a server to protect it, on condition that the agent on the server is online.
   -  Disable WTP before updating a website and enable it after the update is complete. Otherwise, the website will fail to be updated.
   -  Your website is not protected while WTP is disabled. Enable it immediately after updating your website.

Related Operations
------------------

**Disabling WTP**

Choose **Prevention** > **Web Tamper Protection** and click the **Servers** tab. Click **Disable Protection** in the **Operation** column of a server.

.. important::

   -  Before disabling WTP, perform a comprehensive detection on the server, handle known risks, and record operation information to prevent O&M errors and attacks on the server.
   -  If WTP is disabled, web applications are more likely to be tampered with. Therefore, you need to delete important data on the server, stop important services on the server, and disconnect the server from the external network in a timely manner to avoid unnecessary losses caused by attacks on the server.
   -  After you or disable WTP, files in the protected directory are no longer protected. You are advised to process files in the protected directory before performing these operations.
   -  If you find some files missing after disabling WTP, search for them in the local or remote backup path.

   -  The premium edition will be disabled when you disable WTP.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

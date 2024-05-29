:original_name: hss_01_0106.html

.. _hss_01_0106:

Configuring Remote Backup
=========================

By default, HSS backs up the files from the protected directories (excluding specified subdirectories and file types) to the local backup directory you specified when adding protected directories. To protect the local backup files from tampering, you must enable the remote backup function.

If the file and backup directory on the local server become invalid, you can manually obtain the backup file from the remote backup server to restore the tampered websites.

Constraints
-----------

Only the servers that are protected by the HSS WTP edition support the operations described in this section.

Prerequisites
-------------

The following servers can be used as remote backup servers:

Linux servers whose **Server Status** is **Running** and **Agent Status** is **Online**

.. important::

   -  The remote backup function can be used when the Linux backup server is connected to your cloud server. To ensure a proper backup, you are advised to select a backup server on the same intranet as your cloud server.
   -  You are advised to use intranet servers least exposed to attacks as the remote backup servers.

Adding a Remote Backup Server
-----------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

#. Choose **Prevention** > **Web Tamper Protection**, click **Configure Protection**.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.


   .. figure:: /_static/images/en-us_image_0000001854854673.png
      :alt: **Figure 1** Entering the page for protected directory settings

      **Figure 1** Entering the page for protected directory settings

#. Click **Settings** under **Protected Directory Settings**.


   .. figure:: /_static/images/en-us_image_0000001669998725.png
      :alt: **Figure 2** Protected directory settings

      **Figure 2** Protected directory settings

#. Click **Manage Remote Backup**. In the dialog box that is displayed, click **Add Backup Server**. For details, see :ref:`Table 1 <hss_01_0106__table1423774551618>`.


   .. figure:: /_static/images/en-us_image_0000001620839122.png
      :alt: **Figure 3** Adding a Remote Backup Server

      **Figure 3** Adding a Remote Backup Server

   .. _hss_01_0106__table1423774551618:

   .. table:: **Table 1** Backup server parameters

      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                                                                                                                    |
      +===================================+================================================================================================================================================================================================================================================================+
      | Address                           | This address is the private network address of the server.                                                                                                                                                                                                     |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Port                              | Ensure that the port is not blocked by any security group or firewall or occupied.                                                                                                                                                                             |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Backup Path                       | Path of remote backup files.                                                                                                                                                                                                                                   |
      |                                   |                                                                                                                                                                                                                                                                |
      |                                   | -  If the protected directories of multiple servers are backed up to the same remote backup server, the data will be stored in separate folders named after agent IDs.                                                                                         |
      |                                   |                                                                                                                                                                                                                                                                |
      |                                   |    Assume the protected directories of the two servers are **/hss01** and **hss02**, and the agent IDs of the two servers are **f1fdbabc-6cdc-43af-acab-e4e6f086625f** and **f2ddbabc-6cdc-43af-abcd-e4e6f086626f**, and the remote backup path is **/hss01**. |
      |                                   |                                                                                                                                                                                                                                                                |
      |                                   |    The corresponding backup paths are **/hss01/f1fdbabc-6cdc-43af-acab-e4e6f086625f** and **/hss01/f2ddbabc-6cdc-43af-abcd-e4e6f086626f**.                                                                                                                     |
      |                                   |                                                                                                                                                                                                                                                                |
      |                                   | -  If WTP is enabled for the remote backup server, do not set the remote backup path to any directories protected by WTP. Otherwise, remote backup will fail.                                                                                                  |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Click **OK**.

Setting remote backup
---------------------

#. Log in to the management console.

#. Choose **Prevention** > **Web Tamper Protection**, click **Configure Protection**.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.


   .. figure:: /_static/images/en-us_image_0000001854854673.png
      :alt: **Figure 4** Entering the page for protected directory settings

      **Figure 4** Entering the page for protected directory settings

#. Click **Settings** under **Protected Directory Settings**.


   .. figure:: /_static/images/en-us_image_0000001669998725.png
      :alt: **Figure 5** Protected directory settings

      **Figure 5** Protected directory settings

#. Click **Enable Remote Backup** and select a remote backup server.

#. Click **OK** to start remote backup.

Changing a Remote Backup Server
-------------------------------

#. Log in to the management console.

#. Choose **Prevention** > **Web Tamper Protection**, click **Configure Protection**.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.


   .. figure:: /_static/images/en-us_image_0000001854854673.png
      :alt: **Figure 6** Entering the page for protected directory settings

      **Figure 6** Entering the page for protected directory settings

#. Click **Settings** under **Protected Directory Settings**.


   .. figure:: /_static/images/en-us_image_0000001669998725.png
      :alt: **Figure 7** Protected directory settings

      **Figure 7** Protected directory settings

#. Click **Manage Remote Backup Servers**. The **Manage Remote Backup Servers** page is displayed. Click **Edit** in the **Operation** column to modify the information about the remote backup server.

#. Click **OK**.

Related Operations
------------------

**Disabling remote backup**

Exercise caution when performing this operation. If remote backup is disabled, HSS will no longer back up files in your protected directories.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

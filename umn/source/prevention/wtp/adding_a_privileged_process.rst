:original_name: hss_01_0466.html

.. _hss_01_0466:

Adding a Privileged Process
===========================

If WTP is enabled, the content in the protected directories is read-only. To allow certain processes to modify files in the directories, add them to the privileged process list.

Only the modification made by privileged processes can take effect. Modifications made by other processes will be automatically rolled back.

Exercise caution when adding privileged processes. Do not let untrustworthy processes access your protected directories.

Constraints
-----------

-  Only the servers that are protected by the HSS WTP edition support the operations described in this section.
-  For Linux OSs, only x86 OSs with kernel 4.18 support this function.
-  The privileged process takes effect only for Agent 3.2.4 or later.
-  A maximum of 10 privileged processes can be added to each server.

Prerequisites
-------------

The **Protection Status** of the server must be **Protected**. To view the status, choose **Prevention** > **Web Tamper Protection**. Click the **Servers** tab.


Adding a Privileged Process
---------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

#. Choose **Prevention** > **Web Tamper Protection**, click **Configure Protection**.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.


   .. figure:: /_static/images/en-us_image_0000001854854673.png
      :alt: **Figure 1** Entering the page for protected directory settings

      **Figure 1** Entering the page for protected directory settings

#. Click **Privileged Process Settings** and then **Settings**.


   .. figure:: /_static/images/en-us_image_0000001620847478.png
      :alt: **Figure 2** Setting a privileged process

      **Figure 2** Setting a privileged process

#. On the **Privileged Process Settings** page, click **Add Privileged Process**.


   .. figure:: /_static/images/en-us_image_0000001621167210.png
      :alt: **Figure 3** Adding a Privileged Process

      **Figure 3** Adding a Privileged Process

#. In the **Add Privileged Process** dialog box, enter the path of the privileged process.

   The process file path must contain the process name and extension, for example, **C:/Path/Software.type**. If the process has no extension, ensure the process name is unique.

#. Click **OK**.

Related Operations
------------------

**Modifying or deleting existing privileged processes**

In the **Operation** column of a process file path, click **Edit** to modify the privileged processes or click **Delete** to delete it if it is unnecessary.

.. note::

   -  After you edit or delete the process file path, the privileged process cannot modify the files in the protected directory. To avoid impact on services, exercise caution when performing these operations.
   -  Unnecessary privileged processes should be deleted in a timely manner as they may be exploited by attackers.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

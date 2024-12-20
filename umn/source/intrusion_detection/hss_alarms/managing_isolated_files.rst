:original_name: hss_01_0331.html

.. _hss_01_0331:

Managing Isolated Files
=======================

HSS can isolate detected threat files. Files that have been isolated are displayed on a slide-out panel on the **Server Alarms** page. You can click **Isolated Files** on the upper right corner to check them, and can recover isolated files anytime.

For details about events that can be isolated and killed, see :ref:`Server Alarms <hss_01_0277>`.

Constraints
-----------

Servers that are not protected by HSS do not support alarm-related operations.

Isolation and Killing Operations
--------------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane on the left, choose **Intrusion Detection** > **Alarms** and click **Server Alarms**.


   .. figure:: /_static/images/en-us_image_0000001621827002.png
      :alt: **Figure 1** Server alarms

      **Figure 1** Server alarms

#. Locate an event that can be isolated and killed, click **Handle** in the **Operation** column, and select **Isolate and Kill** in the displayed box.

   .. note::

      For details about events that can be isolated and killed, see :ref:`Server Alarms <hss_01_0277>`.

#. Click **OK** and isolate and kill the target alarm event.

   Files that have been isolated are displayed on a slide-out panel on the **Server Alarms** page and cannot harm your servers. You can click **Isolated Files** on the upper right corner to check them.

Checking Isolated Files
-----------------------

#. In the alarm statistics area on the **Server Alarms** page, click **Isolated Files** to check the isolated files.
#. Check the servers, names, paths, and modification time of the isolated files.

Restoring Isolated Files
------------------------

If you want to de-isolate an isolated file, you can restore it by referring to the following steps.

#. Click **Restore** in the **Operation** column of the list. The dialog box is displayed.
#. Click **OK**.

   .. note::

      The permissions for this file will be restored to what they were before it was isolated.

Deleting Isolated Files
-----------------------

If you want to permanently delete an isolated file, you can perform the deletion operation by referring to the following steps.

#. Click **Delete** in the **Operation** column of the list. The dialog box is displayed.

   To delete isolated files in batches, select multiple isolated files and click **Delete** in the upper left corner of the list.

#. Click **OK**.

   .. note::

      Deleted isolated files cannot be restored. Exercise caution when performing this operation.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

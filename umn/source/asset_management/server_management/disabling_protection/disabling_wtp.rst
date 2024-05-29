:original_name: hss_01_0400.html

.. _hss_01_0400:

Disabling WTP
=============

You can disable the WTP edition for a server. A quota that has been unbound from a server can be bound to another one.

Precautions
-----------

Disabling protection does not affect services, but will increase security risks. You are advised to keep your servers protected.

Procedure
---------

#. Log in to the management console.
#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

3. In the navigation pane, choose **Protection** > **Web Tamper Protection**. On the **Web Tamper Protection** page, click the **Servers** tab.


   .. figure:: /_static/images/en-us_image_0000001854854673.png
      :alt: **Figure 1** Entering the page for protected directory settings

      **Figure 1** Entering the page for protected directory settings

4. Click **Disable** in the **Operation** column of a server.

   .. note::

      The WTP edition cannot be disabled for servers in batches.

5. In the dialog box that is displayed, confirm the information and click **OK**.


   .. figure:: /_static/images/en-us_image_0000001782537137.png
      :alt: **Figure 2** Confirming information about disabling WTP

      **Figure 2** Confirming information about disabling WTP

6. Choose **Asset Management** > **Servers & Quota** and click the **Servers** tab. Check the protection status in the server list. If it is **Unprotected**, the protection has been disabled.

   .. caution::

      Disabling protection does not affect services, but will increase security risks. You are advised to keep your servers protected.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

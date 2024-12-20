:original_name: hss_01_0401.html

.. _hss_01_0401:

Disabling Protection for Container Edition
==========================================

You can disable the container edition for a server. A quota that has been unbound from a server can be bound to another one.

Before You Start
----------------

Disabling protection does not affect services, but will increase security risks. You are advised to keep your servers protected.

Disabling the Container Edition
-------------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane, choose **Asset Management** > **Containers & Quota**.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.


   .. figure:: /_static/images/en-us_image_0000001806095454.png
      :alt: **Figure 1** Accessing the container node management page

      **Figure 1** Accessing the container node management page

#. In the **Operation** column of a server, click **Disable Protection**.

   To disable protection in batches, select multiple target servers and click **Disable Protection**.

#. In the dialog box that is displayed, confirm the information and click **OK**.

#. Choose **Asset Management** > **Containers & Quota** and click the **Container Nodes** tab. Check the container protection status in the server list. If it is **Unprotected**, the protection has been disabled.

   .. caution::

      Disabling protection does not affect services, but will increase security risks. You are advised to keep your servers protected.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

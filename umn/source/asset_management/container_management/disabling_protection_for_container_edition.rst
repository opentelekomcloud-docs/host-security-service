:original_name: hss_01_0401.html

.. _hss_01_0401:

Disabling Protection for Container Edition
==========================================

You can disable the container edition for a server. A quota that has been unbound from a server can be bound to another one.

Before You Start
----------------

Disabling protection does not affect services, but will increase security risks. You are advised to keep your servers protected.

Procedure
---------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

#. In the navigation pane, choose **Asset Management** > **Containers & Quota**.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.


   .. figure:: /_static/images/en-us_image_0000001806095454.png
      :alt: **Figure 1** Accessing the container node management page

      **Figure 1** Accessing the container node management page

#. Disable protection for one or multiple servers.

   -  **Disabling protection for a server**

      a. In the node list, click **Disable Protection** in the **Operation** column of a server.
      b. In the dialog box that is displayed, confirm the information and click **OK**.
      c. Choose **Asset Management** > **Containers & Quota** and click the **Container Nodes** tab. Check the protection status in the server list. If it is **Unprotected**, the protection has been disabled.

         .. caution::

            Disabling protection does not affect services, but will increase security risks. You are advised to keep your servers protected.

   -  **Disabling protection in batches**

      a. In the node list, select servers, and click **Disable Protection** above the list.
      b. In the dialog box that is displayed, confirm the information and click **OK**.
      c. Choose **Asset Management** > **Containers & Quota** and click the **Container Nodes** tab. Check the protection status in the server list. If it is **Unprotected**, the protection has been disabled.

         .. caution::

            Disabling protection does not affect services, but will increase security risks. You are advised to keep your servers protected.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

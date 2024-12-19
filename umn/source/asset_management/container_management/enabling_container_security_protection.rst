:original_name: hss_01_0398.html

.. _hss_01_0398:

Enabling Container Security Protection
======================================

You can enable the container security edition for your containers.

To enable protection for a container node, you need to allocate a quota to the node. If the protection is disabled or the node is deleted, the quota can be allocated to another node.

Check Frequency
---------------

HSS performs a full check in the early morning every day.

After you enable server protection, you can view scan results after the automatic scan at 04:10 in the next morning.

Prerequisite
------------

-  On the **Container Nodes** tab of the **Asset Management** > **Containers & Quota** page, the **Agent Status** of a server is **Online**, and the **Protection Status** of the server is **Unprotected**.
-  You have created a node on CCE.

Procedure
---------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane, choose **Asset Management** > **Containers & Quota**.


   .. figure:: /_static/images/en-us_image_0000001782558509.png
      :alt: **Figure 1** Accessing the container node management page

      **Figure 1** Accessing the container node management page

#. Enable protection for one or multiple servers.

   -  **Enabling protection for a server**

      a. In the **Operation** column of a server, click **Enable Protection**.
      b. In the dialog box that is displayed, confirm the information.

         .. note::

            A container security quota protects one cluster node.

      c. Confirm the information and click **OK**. If the **Protection Status** in the container list changes to **Protected**, it indicates the protection has been enabled.

   -  **Enabling protection in batches**

      a. In the node list, select servers, and click **Enable Protection** above the list.
      b. In the dialog box that is displayed, confirm the information.

         .. note::

            A container security quota protects one cluster node.

      c. Confirm the information and click **OK**. If the **Protection Status** in the container list changes to **Protected**, it indicates the protection has been enabled.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

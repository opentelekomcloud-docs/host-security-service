:original_name: hss_01_0295.html

.. _hss_01_0295:

Enabling Container Protection
=============================

Before enabling protection for a container node, you need to allocate quota to a specified node. If the protection is disabled or the node is deleted, the quota can be allocated to other nodes.

Check Frequency
---------------

HSS performs a full check in the early morning every day.

After you enable server protection, you can view scan results after the automatic scan in the next early morning.

Prerequisites
-------------

-  On the HSS console, choose **Asset Management** > **Containers & Quota**. The **Agent Status** of the node is **Online** and the **Protection Status** is **Unprotected**.
-  You have created nodes on CCE.

Procedure
---------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane, choose **Asset Management** > **Containers & Quota**.


   .. figure:: /_static/images/en-us_image_0000001735474790.png
      :alt: **Figure 1** Accessing the container node management page

      **Figure 1** Accessing the container node management page

#. In the **Operation** column of the node list, click **Enable Protection**.

#. In the displayed dialog box, confirm the server information.

#. Click **OK**. If the **Protection Status** of the server changes to **Protected**, protection has been enabled.

   .. note::

      A container security quota protects one cluster node.

Related Operations
------------------

**Disabling protection for a node**

Choose **Asset Management** > **Containers & Quota**, click the **Container Nodes** tab, and click **Nodes**. In the **Operation** column, click **Disable Protection**.

.. important::

   -  Before disabling protection, perform a comprehensive detection on the container, handle detected risks, and record operation information to prevent O&M errors and attacks on the container.
   -  After protection is disabled, clear important data on the container, stop important applications on the container, and disconnect the container from the external network to avoid unnecessary loss caused by attacks.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

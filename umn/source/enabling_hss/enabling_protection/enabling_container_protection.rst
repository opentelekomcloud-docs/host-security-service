:original_name: hss_01_0293.html

.. _hss_01_0293:

Enabling Container Protection
=============================

Before enabling protection for a container node, you need to allocate quota to a specified node. If the protection is disabled or the node is deleted, the quota can be allocated to other nodes.

Check Frequency
---------------

HSS performs a full check in the early morning every day.

After you enable server protection, you can view scan results after the automatic scan in the next early morning.

Prerequisites
-------------

-  The **Agent Status** of a server is **Online**. To check the status, choose **Asset Management** > **Containers & Quota**.
-  You have created nodes on CCE.
-  The **Protection Status** of the node is **Unprotected**.

Procedure
---------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

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

If protection is disabled, the quota status will change from occupied to idle. You can allocate the idle quota to another node to avoid quota waste.

.. important::

   -  Before disabling protection, perform a comprehensive detection on the container, handle detected risks, and record operation information to prevent O&M errors and attacks on the container.
   -  After protection is disabled, clear important data on the container, stop important applications on the container, and disconnect the container from the external network to avoid unnecessary loss caused by attacks.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

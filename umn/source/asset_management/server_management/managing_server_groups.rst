:original_name: hss_01_0023.html

.. _hss_01_0023:

Managing Server Groups
======================

To manage servers by group, you can create a server group and add servers to it.

You can check the numbers of servers, unsafe servers, and unprotected servers in a group.

Creating a Server Group
-----------------------

After creating a server group, you can add servers to the group for unified management.

#. Log in to the management console.
#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

3. In the navigation pane, choose **Asset Management** > **Servers & Quota**, click **Server Groups** in the **Server** list, and click **Create Server Group**.


   .. figure:: /_static/images/en-us_image_0000001711689404.png
      :alt: **Figure 1** Accessing the page of server groups

      **Figure 1** Accessing the page of server groups

4. In the **Create Server Group** dialog box, enter a server group name and select the servers to be added to the group.

   .. note::

      -  A server group name must be unique, or the group will fail to be created.
      -  A name cannot contain spaces. It contains only letters, digits, underscores (_), hyphens (-), dots (.), asterisks (*), and plus signs (+). The length cannot exceed 64 characters.


   .. figure:: /_static/images/en-us_image_0000001735592920.png
      :alt: **Figure 2** Creating a server group

      **Figure 2** Creating a server group

5. Click **OK**.

Adding Servers to Groups
------------------------

You can add servers to an existing server group.

#. Click the **Server** tab.

#. Select one or more servers and click **Add to Group**.


   .. figure:: /_static/images/en-us_image_0000001735433752.png
      :alt: **Figure 3** Adding servers to a group

      **Figure 3** Adding servers to a group

   .. note::

      To add a server to a group, you can also locate the row where the server resides, click **More** in the **Operation** column, and choose **Add to Group**.

#. In the displayed dialog box, select a server group and click **OK**.

   .. note::

      A server can be added to only one server group.

Related Operations
------------------

**Editing a server group**

#. Click **Servers & Quota** and click **Server Groups** on the **Servers** tab.
#. Locate the row where a server group resides and click **Edit** in the **Operation** column.
#. In the displayed dialog box, change the server group name and add or remove servers in the group.
#. Click **OK**.

**Deleting a server group**

#. Click **Servers & Quota** and click **Server Groups** on the **Servers** tab.
#. Locate the row where a server group resides and click **Delete** in the **Operation** column.

   .. note::

      After the server group is deleted, the **Server Group** column of the servers that were in the group will be blank.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

:original_name: hss_01_0624.html

.. _hss_01_0624:

Configuring a Network Defense Policy (for a Cluster Using the VPC Tunnel Network Model)
=======================================================================================

For clusters using the VPC network model, you can configure network defense policies to limit the traffic that accesses the servers where containers are deployed. If no security group rules are configured, all incoming and outgoing traffic of the servers is allowed by default.

This section describes how to configure a network defense policy for a cluster using the VPC network model.

Creating a Network Defense Policy
---------------------------------

#. Log in to the management console.
#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

3. In the navigation pane on the left, choose **Prevention** > **Container Firewalls**.

4. Click **Synchronize** above the cluster list to synchronize the policies created on CCE.

   The synchronization takes about 1 to 2 minutes. Wait for a while and click |image2| in the upper right corner of the list to refresh and view the latest data.

5.  Click **Manage Policy** in the **Operation** column of a cluster using the VPC network model.

6.  In the **Operation** column of a node, click **Configure Policy**.

7.  In the displayed dialog box, click **OK** to go to the cloud server console.

8.  Click the **Security Groups** tab and view security group rules.

9.  Click the security group ID. The system automatically switches to the security group page.

10. Configure inbound and outbound rules.

    For details, see "Adding a Security Group Rule" in *Virtual Private Cloud User Guide*.

Related Operations
------------------

**Modifying or deleting a network defense policy**

#. Go to the console.
#. In the navigation pane on the left, choose **Prevention** > **Container Firewalls**.
#. Click **Manage Policy** in the **Operation** column of a cluster using the VPC network model.
#. Click **Synchronize** above the node list to synchronize node information.
#. Check the value of **Last synchronized**. If it changes to the completion time of the latest synchronization task, the synchronization is complete.
#. In the **Operation** column of a node, click **Configure Policy**.
#. In the displayed dialog box, click **OK** to go to the cloud server console.
#. Click the **Security Groups** tab and view security group rules.
#. Click the server name or ID. The basic information page of the server name is displayed.
#. Click a rule tab and manage rules as needed.

   -  Modifying a rule

      In the **Operation** column of a rule, click **Modify**. Modify the rule and click **OK**.

   -  Deleting a rule

      In the **Operation** column of a rule, click **Delete**. In the confirmation dialog box, click **OK**.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png
.. |image2| image:: /_static/images/en-us_image_0000001891447456.png

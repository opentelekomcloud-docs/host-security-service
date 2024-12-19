:original_name: hss_01_0634.html

.. _hss_01_0634:

Disabling Container Cluster Protection
======================================

If you no longer need HSS to protect your container clusters, you can disable container cluster protection.


Disabling Container Cluster Protection
--------------------------------------

#. Log in to the management console.

2. In the navigation pane, choose **Prevention** > **Container Cluster Protection**.

3. Click the **Protected Clusters** tab.

4. In the **Operation** column of a cluster, click **Disable Protection**.

   To disable protection for clusters in batches, select clusters and click **Disable Protection** in the upper left corner of the cluster list.

5. In the dialog box that is displayed, determine whether to select the **Delete policy plug-in of the cluster** check box.

   -  If you select it, container cluster protection policies and the policy configuration plug-in will be deleted. If you enable protection again, you will need to install the policy configuration plug-in and configure protection policies again.
   -  If you deselect it, container cluster protection policies will be deleted but the policy configuration plug-in will be retained. If you enable protection again, you only need to configure protection policies. If you want to delete the policy configuration plug-in later, repeat the preceding steps to disable protection and select **Delete policy plug-in of the cluster**.

6. Click **OK**.

   -  If you did not select **Delete policy plug-in of the cluster** and the **Protection Status** of the cluster changes to **Enabled but not configured**, it indicates protection has been disabled.
   -  If you selected **Delete policy plug-in of the cluster** and the **Protection Status** of the cluster changes to **Unprotected**, it indicates protection has been disabled.

:original_name: hss_01_0631.html

.. _hss_01_0631:

Enabling Container Cluster Protection
=====================================

Container cluster protection can detect risks in baselines, vulnerabilities, and malicious files; and can report alarms on or block insecure container images. You can enable protection to enhance cluster defense and protect containers.

Constraints
-----------

After container cluster protection is enabled, you need to configure a policy to make the protection take effect. For more information, see :ref:`Configuring a Container Cluster Protection Policy <hss_01_0632>`.


Enabling Container Cluster Protection
-------------------------------------

#. Log in to the management console.

2. In the navigation pane, choose **Prevention** > **Container Cluster Protection**.

3. Click the **Protected Clusters** tab.

4. Click **Synchronize** to synchronize clusters.

5. Click **Enable** in the **Operation** column of a cluster.

   To enable protection for clusters in batches, select clusters and click **Enable Protection** in the upper left corner of the cluster list.

   .. important::

      -  After container cluster protection is enabled for a cluster, the policy management plug-in will be installed in the cluster and occupy some cluster resources.
      -  When enabling protection for a container cluster, do not perform any operation on the cluster. Otherwise, protection will fail to be enabled.

6. Click **OK**.

   If the **Protection Status** of the container cluster is **Enabled but not configured**, it indicates protection has been configured for the cluster and the policy management plug-in has been installed, but HSS has not started to protect your cluster. In this case, you need to configure a protection policy. For more information, see :ref:`Configuring a Container Cluster Protection Policy <hss_01_0632>`.

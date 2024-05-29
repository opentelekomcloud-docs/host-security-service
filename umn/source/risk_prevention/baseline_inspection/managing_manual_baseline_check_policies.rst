:original_name: hss_01_0393.html

.. _hss_01_0393:

Managing Manual Baseline Check Policies
=======================================

This section describes how to modify a created manual baseline check policy.

Editing a Manual Baseline Check Policy
--------------------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

#. In the navigation pane on the left, choose **Prediction** > **Baseline Checks**.


   .. figure:: /_static/images/en-us_image_0000001618285045.png
      :alt: **Figure 1** Baseline check overview

      **Figure 1** Baseline check overview

4. Click **Policies** in the upper right corner of the page.


   .. figure:: /_static/images/en-us_image_0000001743828960.png
      :alt: **Figure 2** Baseline policies

      **Figure 2** Baseline policies

5. Click **Edit** in the **Operation** column of a policy. On the policy details page that is displayed, configure the policy name and check items.

   .. note::

      If you select **Linux** for **OS**, you can select any checks included in **Baseline** and edit rules. This function is not supported for Windows servers.


   .. figure:: /_static/images/en-us_image_0000001618325933.png
      :alt: **Figure 3** Editing a baseline check policy

      **Figure 3** Editing a baseline check policy

6. Confirm the configuration, click **Next**, and select servers.

7. Confirm the information and click **OK**. You can view the updated policy in the policy list.

Deleting a Manual Baseline Check Policy
---------------------------------------

#. Log in to the management console.

#. Click |image2| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

#. In the navigation pane on the left, choose **Prediction** > **Baseline Checks**.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.


   .. figure:: /_static/images/en-us_image_0000001618285045.png
      :alt: **Figure 4** Baseline check overview

      **Figure 4** Baseline check overview

#. Click **Policies** in the upper right corner of the page.


   .. figure:: /_static/images/en-us_image_0000001743828960.png
      :alt: **Figure 5** Baseline policies

      **Figure 5** Baseline policies

#. Click **Delete** in the **Operation** column of a policy. In the dialog box that is displayed, confirm the information and click **OK**.

   .. note::

      Only user-defined policies can be deleted. Default policies **default_linux_security_check_policy** and **default_windows_security_check_policy** cannot be deleted.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png
.. |image2| image:: /_static/images/en-us_image_0000001517477398.png

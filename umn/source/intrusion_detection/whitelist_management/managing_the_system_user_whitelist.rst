:original_name: hss_01_0496.html

.. _hss_01_0496:

Managing the System User Whitelist
==================================

HSS generates risky account alarms when non-root users are added to the root user group. You can add the trusted non-root users to the system user whitelist. HSS does not generate risky account alarms for users in the system user whitelist.

Procedure
---------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

#. In the navigation pane on the left, choose **Detection** > **Whitelists**. The **Whitelists** page is displayed.

#. (Optional) In the upper left corner of the **Whitelists** page, select the enterprise project to which the server belongs or **All projects** for **Enterprise Project**.

   If you have not enabled the enterprise project function, skip this step.

#. Click the **System User Whitelist** tab and click **Add**.


   .. figure:: /_static/images/en-us_image_0000001853795117.png
      :alt: **Figure 1** Configuring the system user whitelist

      **Figure 1** Configuring the system user whitelist

#. In the **Add to System User Whitelist** dialog box, enter the server ID, system username, and remarks.

#. Click **OK**.

Related Operations
------------------

**Modifying a System User Whitelist**

#. (Optional) In the upper left corner of the **Whitelists** page, select the enterprise project to which the server belongs or **All projects** for **Enterprise Project**.

   If you have not enabled the enterprise project function, skip this step.

#. In the row of the target system user whitelist, click **Modify** in the **Operation** column.

#. In the **Modify System User Whitelist** dialog box, modify the information and click **OK**.

**Deleting a System User Whitelist**

#. In the row of the target system user whitelist, click **Delete** in the **Operation** column.

   You can also select multiple system user whitelists and click **Delete** in the upper left corner of the system user whitelist list.

#. In the dialog box displayed, click **OK**.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

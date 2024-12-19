:original_name: hss_01_0618.html

.. _hss_01_0618:

Managing Security Reports
=========================

You can modify, cancel, or unsubscribe to a report.

Constraints
-----------

The enterprise, premium, WTP, or container edition is enabled.

.. _hss_01_0618__hss_01_0557_section341765792112:

Editing a Report
----------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane on the left, choose **Reports**. The security report overview page is displayed.

   You can use default security report templates directly, which are **default monthly security report** and **default weekly security report**.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.


   .. figure:: /_static/images/en-us_image_0000001670240689.png
      :alt: **Figure 1** Checking a security report

      **Figure 1** Checking a security report

#. Click **Edit** in the lower right corner of the target report.


   .. figure:: /_static/images/en-us_image_0000001622361502.png
      :alt: **Figure 2** Editing a report

      **Figure 2** Editing a report

#. Edit basic information of a report. For more information, see :ref:`Table 1 <hss_01_0618__hss_01_0557_table164462775520>`.


   .. figure:: /_static/images/en-us_image_0000001670401553.png
      :alt: **Figure 3** Editing basic information of a report

      **Figure 3** Editing basic information of a report

   .. _hss_01_0618__hss_01_0557_table164462775520:

   .. table:: **Table 1** Parameter description

      +-----------------------+---------------------------------------------------------------------------------------------------------------------------------+-------------------------------------+
      | Parameter             | Description                                                                                                                     | Example Value                       |
      +=======================+=================================================================================================================================+=====================================+
      | Report Name           | Default report name.                                                                                                            | **default monthly security report** |
      +-----------------------+---------------------------------------------------------------------------------------------------------------------------------+-------------------------------------+
      | Report Type           | Name of the statistical period type of a report, which cannot be edited.                                                        | **Monthly Reports**                 |
      +-----------------------+---------------------------------------------------------------------------------------------------------------------------------+-------------------------------------+
      | Schedule Delivery     | Time when a report is automatically sent.                                                                                       | ``-``                               |
      +-----------------------+---------------------------------------------------------------------------------------------------------------------------------+-------------------------------------+
      | Send Report To        | Security report recipients.                                                                                                     | Recipients specified in SMN topic   |
      |                       |                                                                                                                                 |                                     |
      |                       | -  **Recipients specified in SMN topic**: If you use SMN topic settings, you can create a topic and specify recipients for HSS. |                                     |
      |                       | -  **No need to send to email**: The report is not sent to the specified email address.                                         |                                     |
      +-----------------------+---------------------------------------------------------------------------------------------------------------------------------+-------------------------------------+

#. Confirm the information and click **Next** in the lower right corner of the page to configure the report.

#. Select or deselect the report items in the pane on the left. You can preview the report items on the right. After confirming the report items, click **Save**. The report is changed successfully.

Enabling or Disabling Subscription
----------------------------------

#. Log in to the management console and go to the HSS page.

#. In the navigation pane on the left, choose **Reports**. The security report overview page is displayed.

   You can use default security report templates directly, which are **default monthly security report** and **default weekly security report**.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.


   .. figure:: /_static/images/en-us_image_0000001670240689.png
      :alt: **Figure 4** Checking a security report

      **Figure 4** Checking a security report

#. Click the switch in the upper right corner of a report to enable or disable the subscription.

   -  |image2|: The subscription is disabled and no reports will be generated.

Deleting a Report
-----------------

.. note::

   Default security report templates **default monthly security report** and **default weekly security report** cannot be deleted.

#. Log in to the management console and go to the HSS page.

#. In the navigation pane on the left, choose **Reports**. The security report overview page is displayed.

   You can use default security report templates directly, which are **default monthly security report** and **default weekly security report**.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.


   .. figure:: /_static/images/en-us_image_0000001670240689.png
      :alt: **Figure 5** Checking a security report

      **Figure 5** Checking a security report

#. Click **Delete** in the lower right corner of the target report.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png
.. |image2| image:: /_static/images/en-us_image_0000001901831352.png

:original_name: hss_01_0615.html

.. _hss_01_0615:

Creating a Security Report
==========================

If the type and content of the existing report template cannot meet your requirements, you can customize a report.

Constraints
-----------

The enterprise, premium, WTP, or container edition is enabled.


Creating a Security Report
--------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane on the left, choose **Reports**. The security report overview page is displayed.

   You can use default security report templates directly, which are **default monthly security report** and **default weekly security report**.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.


   .. figure:: /_static/images/en-us_image_0000001670240689.png
      :alt: **Figure 1** Checking a security report

      **Figure 1** Checking a security report

#. Create a report.

   -  Create a monthly or weekly security report based on templates.

      -  Click **Copy** in the weekly or monthly report card to access the basic information configuration page.


         .. figure:: /_static/images/en-us_image_0000001670375709.png
            :alt: **Figure 2** Creating a report based on a template

            **Figure 2** Creating a report based on a template

   -  .. _hss_01_0615__hss_01_0556_li77667419127:

      You can also customize the report period.

      -  Click **Create Report** to access the basic information configuration page.


         .. figure:: /_static/images/en-us_image_0000001622521482.png
            :alt: **Figure 3** Customizing a report

            **Figure 3** Customizing a report

#. Edit basic information of a report. For more information, see :ref:`Table 1 <hss_01_0615__hss_01_0556_table164462775520>`.


   .. figure:: /_static/images/en-us_image_0000001670681377.png
      :alt: **Figure 4** Editing basic information of a report

      **Figure 4** Editing basic information of a report

   .. _hss_01_0615__hss_01_0556_table164462775520:

   .. table:: **Table 1** Parameter description

      +-----------------------+---------------------------------------------------------------------------------------------------------------------------------+-----------------------------------+
      | Parameter             | Description                                                                                                                     | Example Value                     |
      +=======================+=================================================================================================================================+===================================+
      | Report Name           | Default report name                                                                                                             | ecs security report               |
      +-----------------------+---------------------------------------------------------------------------------------------------------------------------------+-----------------------------------+
      | Report Type           | Statistical period type of a report:                                                                                            | Monthly Reports                   |
      |                       |                                                                                                                                 |                                   |
      |                       | -  **Daily**: 00:00 to 24:00 every day                                                                                          |                                   |
      |                       | -  **Weekly Reports**: 00:00 on Monday to 24:00 on Sunday                                                                       |                                   |
      |                       | -  **Monthly Reports**: 00:00 on the first day to 24:00 on the last day of each month                                           |                                   |
      |                       | -  **Custom**: custom statistical period, which ranges from one day to three months                                             |                                   |
      |                       | -  All types of reports will be sent to the recipients the day after it is generated.                                           |                                   |
      +-----------------------+---------------------------------------------------------------------------------------------------------------------------------+-----------------------------------+
      | Schedule Delivery     | Time when a report is automatically sent                                                                                        | ``-``                             |
      +-----------------------+---------------------------------------------------------------------------------------------------------------------------------+-----------------------------------+
      | Send Report To        | Security report recipients.                                                                                                     | Recipients specified in SMN topic |
      |                       |                                                                                                                                 |                                   |
      |                       | -  **Recipients specified in SMN topic**: If you use SMN topic settings, you can create a topic and specify recipients for HSS. |                                   |
      |                       | -  **No need to send to email**: The report is not sent to the specified email address.                                         |                                   |
      +-----------------------+---------------------------------------------------------------------------------------------------------------------------------+-----------------------------------+

#. After confirming that the information is correct, click **Next** in the lower right corner of the page to configure the report.

#. Select the report items to be generated in the left pane. You can preview the report items in the right pane. After confirming the report items, click **Save**, and enable security report subscription.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

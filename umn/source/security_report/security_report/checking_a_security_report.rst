:original_name: hss_01_0617.html

.. _hss_01_0617:

Checking a Security Report
==========================

You can check :ref:`daily <hss_01_0615__hss_01_0556_li77667419127>`, weekly, monthly, and :ref:`custom <hss_01_0615__hss_01_0556_li77667419127>` reports. The reports show your server security trends and key security events and risks.

This section describes how to view the generated reports.

.. note::

   -  If you have enabled the enterprise project function, you can select your enterprise project from the **Enterprise project** drop-down list and subscribe to the security report of the project. You can also select **All projects** and subscribe to the security report of servers in all the projects in this region.
   -  After a daily report is created, you can view and download it the next day.

Constraints
-----------

The enterprise, premium, WTP, or container edition is enabled.

Security Report Overview
------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane on the left, choose **Reports**. The security report overview page is displayed.

   You can use default security report templates directly, which are **default monthly security report** and **default weekly security report**.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.


   .. figure:: /_static/images/en-us_image_0000001670240689.png
      :alt: **Figure 1** Checking a security report

      **Figure 1** Checking a security report

#. Click **Download** to go to the preview page. You can check the information of the target report and download or send it.

Checking Report History
-----------------------

The report history stores the report sending details.

#. In the upper right corner of the security report overview page, click **Report History** to check the report sending records.

#. Check the report history on the displayed page, as shown in the following picture. For more information, see :ref:`Table 1 <hss_01_0617__hss_01_0554_table610843618296>`.


   .. figure:: /_static/images/en-us_image_0000001621481094.png
      :alt: **Figure 2** Report sending details

      **Figure 2** Report sending details

   .. _hss_01_0617__hss_01_0554_table610843618296:

   .. table:: **Table 1** Parameter description

      +-----------------------------------+-------------------------------------------+
      | Parameter                         | Description                               |
      +===================================+===========================================+
      | Report Name                       | Name of a sent report.                    |
      +-----------------------------------+-------------------------------------------+
      | Statistical Period                | Statistical period of a sent report.      |
      +-----------------------------------+-------------------------------------------+
      | Report Type                       | Statistical period type of a sent report. |
      |                                   |                                           |
      |                                   | -  Weekly Reports                         |
      |                                   | -  Monthly Reports                        |
      |                                   | -  Daily Reports                          |
      |                                   | -  Custom Reports                         |
      +-----------------------------------+-------------------------------------------+
      | Sent                              | Time when the report is sent.             |
      +-----------------------------------+-------------------------------------------+

#. Click **Download** in the **Operation** column to check historical reports. You can also preview and download the reports.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

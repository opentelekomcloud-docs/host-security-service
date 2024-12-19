:original_name: hss_01_0305.html

.. _hss_01_0305:

Viewing SWR Image Repository Vulnerabilities
============================================

This section describes how to view SWR image repository vulnerabilities and fix the vulnerabilities as prompted.

Prerequisites
-------------

Container node protection has been enabled.

Constraints
-----------

Only vulnerabilities in Linux images can be checked.

Viewing Vulnerabilities in SWR Images
-------------------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation tree on the left, choose **Prediction** > **Container Images**.

#. Click the **SWR Image Repository Vulnerability** tab to view the system and application vulnerability lists. For details about the vulnerability list, see :ref:`SWR image repository vulnerability parameters <hss_01_0305__table12676743184714>`

   .. _hss_01_0305__table12676743184714:

   .. table:: **Table 1** SWR image repository vulnerability parameters

      +------------------------------+----------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                    | Description                                                                                                                      |
      +==============================+==================================================================================================================================+
      | Vulnerability Name           | You can click a vulnerability name to view basic information about a vulnerability and the images affected by the vulnerability. |
      +------------------------------+----------------------------------------------------------------------------------------------------------------------------------+
      | Repair Urgency               | You are advised to fix vulnerabilities of the high and medium levels.                                                            |
      +------------------------------+----------------------------------------------------------------------------------------------------------------------------------+
      | Historically Affected Images | Images affected by the vulnerability.                                                                                            |
      +------------------------------+----------------------------------------------------------------------------------------------------------------------------------+
      | Solution                     | HSS provides a recommended solution to the vulnerability. Click the solution description to go to the details page.              |
      +------------------------------+----------------------------------------------------------------------------------------------------------------------------------+

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

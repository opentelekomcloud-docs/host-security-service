:original_name: hss_01_0305.html

.. _hss_01_0305:

Image Vulnerabilities
=====================

This section describes how to check the vulnerabilities on the private image and determine whether to ignore the vulnerabilities.

Prerequisites
-------------

Container node protection has been enabled.

Constraints
-----------

Only vulnerabilities in Linux images can be checked.

Viewing Vulnerabilities in Private Images
-----------------------------------------

#. Log in to the management console and go to the HSS page.

#. In the navigation pane on the left, choose **Prediction** > **Container Images**. On the displayed page, click **Image Vulnerabilities** and click **Private Image Vulnerabilities** to view private image vulnerabilities.

   .. note::

      Click a risky image to check its vulnerability overview, including the vulnerability name, urgency, status, the number of affected images, and vulnerability description.


   .. figure:: /_static/images/en-us_image_0000001808243728.png
      :alt: **Figure 1** Viewing vulnerabilities in private images

      **Figure 1** Viewing vulnerabilities in private images

   .. table:: **Table 1** Parameter description

      +------------------------------+-----------------------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                    | Description                                                     | Operation                                                                                                                                          |
      +==============================+=================================================================+====================================================================================================================================================+
      | Vulnerability Name           | ``-``                                                           | -  Click |image1| to view the details of a vulnerability, including **CVE ID**, **CVSS Score**, **Disclosed**, and **Vulnerability Details**.      |
      |                              |                                                                 | -  Click the name of a vulnerability to view the images affected by the vulnerability. For details, see :ref:`3 <hss_01_0305__li197631039152513>`. |
      +------------------------------+-----------------------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------+
      | Repair Urgency               | Shows whether the vulnerability should be repaired immediately. | ``-``                                                                                                                                              |
      +------------------------------+-----------------------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------+
      | Historically Affected Images | Shows the number of images that have been affected.             | ``-``                                                                                                                                              |
      +------------------------------+-----------------------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------+
      | Solution                     | Provides a solution to fix the vulnerability.                   | Click the link in the **Solution** column to view the solution.                                                                                    |
      +------------------------------+-----------------------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------+

#. .. _hss_01_0305__li197631039152513:

   Click the vulnerability name to view its basic information and affected images.

.. |image1| image:: /_static/images/en-us_image_0000001517637590.png

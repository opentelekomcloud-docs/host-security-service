:original_name: hss_01_0198.html

.. _hss_01_0198:

How Do I Handle Unsafe Configurations?
======================================

HSS automatically performs a configuration detection for servers. You can repair unsafe configuration items or ignore the configuration items you trust based on the detection result.

-  Modifying unsafe configuration items

   View details about a detection rule, verify the detection result based on the audit description, and handle the exception based on the modification recommendation.

   You are advised to repair the configurations with a high threat level immediately. The configurations with a medium or low threat level can be fixed later based on service requirements.

-  Ignoring trusted configuration items

   #. Click the name of an ECS to view its details. Choose **Baseline Checks** > **Unsafe Configurations**.

   #. Locate the target risk item, click |image1| in front of its name to expand the check items and click **Ignore** in the **Operation** column. You can also select multiple detection rules and click **Ignore** in the upper part of the page to ignore them in batches.

      To unignore an ignored detection rule, click **Unignore** in the **Operation** column. You can also select multiple ignored detection rules and click **Unignore** in the upper part of the page to unignore them in batches.

-  Verification

   After modifying configuration items, you are advised to choose **Prediction** > **Vulnerabilities** and click **Scan** to perform manual scan immediately to verify the result.

.. |image1| image:: /_static/images/en-us_image_0000001568437337.png

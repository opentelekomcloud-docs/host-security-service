:original_name: hss_01_0198.html

.. _hss_01_0198:

How Do I Handle Unsafe Configurations?
======================================

HSS automatically performs a configuration detection for servers. You can repair unsafe configuration items or ignore the configuration items you trust based on the detection result.

-  Modifying unsafe configuration items

   View details about a detection rule, verify the detection result based on the audit description, and handle the exception based on the modification recommendation.

   You are advised to repair the configurations with a high threat level immediately. The configurations with a medium or low threat level can be fixed later based on service requirements.

-  Ignoring trusted configuration items

   #. Log in to the management console.

   #. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**.

   #. In the navigation pane, choose **Asset Management** > **Servers & Quota**.

      .. note::

         If your servers are managed by enterprise projects, you can select the target enterprise project to view or operate the asset and detection information.

   #. On the **Servers** tab, click the name of a server to view its details. Choose **Baseline Checks** > **Unsafe Configurations**.

   #. Locate a baseline item, click |image2| in front of its name to expand the check items, and click **Ignore** in the **Operation** column of an item. You can also select multiple detection rules and click **Ignore** in the upper part of the page to ignore them in batches.

      |image3|

      To unignore an ignored detection rule, click **Unignore** in the **Operation** column. You can also select multiple ignored detection rules and click **Unignore** in the upper part of the page to unignore them in batches.

-  Verification

   After a configuration item is fixed, you are advised to click **Verify** in the **Operation** column. After the verification, check the fix result.

.. |image1| image:: /_static/images/en-us_image_0000001972125950.png
.. |image2| image:: /_static/images/en-us_image_0000001568437337.png
.. |image3| image:: /_static/images/en-us_image_0000002115937137.png

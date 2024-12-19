:original_name: hss_01_0174.html

.. _hss_01_0174:

Switching the HSS Quota Edition
===============================

You can switch the quota edition of a server to the enterprise or premium edition as needed.

Precautions
-----------

You can switch to the enterprise or premium edition.

Prerequisites
-------------

-  Choose **Asset Management** > **Servers & Quota** page. On the **Servers** tab, the protection status of a server is **Protected**.
-  Before switching to a lower edition, check the server, handle known risks, and record operation information to prevent O&M errors and attacks.


Switching the HSS Quota Edition
-------------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane, choose **Asset Management** > **Servers & Quota**. Click the **Servers** tab.


   .. figure:: /_static/images/en-us_image_0000001801549361.png
      :alt: **Figure 1** Server list

      **Figure 1** Server list

4. In the **Operation** column of a server, click **Switch Edition**.

   .. important::

      -  If HSS is switched from a higher edition to a lower edition, protected servers will be more vulnerable to attacks.
      -  You can switch from other editions to the enterprise, or premium edition. To use the WTP edition, you need to purchase and enable it separately.

5. Click **OK**.

   The edition information in the **Edition** column will be updated. If the edition information in the **Edition** column is updated, the HSS edition switch succeeded.

Follow-up Procedure
-------------------

-  After the edition is switched, you can allocate the idle edition quota to other servers.
-  After switching to a lower edition, clear important data on the server, stop important applications on the server, and disconnect the server from the external network to avoid unnecessary loss caused by attacks.
-  After switching to a higher edition, perform a security detection on the server, handle security risks on the server, and configure necessary functions in a timely manner.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

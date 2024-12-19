:original_name: hss_01_0566.html

.. _hss_01_0566:

Configuring Server Login Protection
===================================

You can configure common login locations, common login IP addresses, and an SSH login IP address whitelist.

Configuring Common Login Locations
----------------------------------

After you configure common login locations, HSS will generate alarms on the logins from other login locations. A server can be added to multiple login locations.

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. Choose **Installation & Configuration** and click the **Security Configuration** tab. Click **Common Login Locations** and click **Add Common Login Location**.


   .. figure:: /_static/images/en-us_image_0000001782456353.png
      :alt: **Figure 1** Adding a common login location

      **Figure 1** Adding a common login location

#. In the dialog box that is displayed, select a geographical location and select servers. Confirm the information and click **OK**.


   .. figure:: /_static/images/en-us_image_0000001862392000.png
      :alt: **Figure 2** Configuring common login locations

      **Figure 2** Configuring common login locations

#. Return to the **Security Configuration** tab of the **Installation & Configuration** page. Check whether the added locations are displayed on the **Common Login Locations** subtab.

   .. note::

      HSS has a learning process for remote login alarms. Therefore, after common login locations are added, the first three login locations are regarded as common login locations, and alarms are generated only for the fourth and subsequent non-common login locations.

Configuring Common Login IP Addresses
-------------------------------------

After you configure common IP addresses, HSS will generate alarms on the logins from other IP addresses.

#. Log in to the management console.

#. Click |image2| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. Choose **Installation & Configuration** and click the **Security Configuration** tab. Click **Common Login IP Addresses** and click **Add Common Login IP Address**.


   .. figure:: /_static/images/en-us_image_0000002087633353.png
      :alt: **Figure 3** Adding a common login IP address

      **Figure 3** Adding a common login IP address

4. In the dialog box that is displayed, enter an IP address and select servers. Confirm the information and click **OK**.

   .. note::

      -  A common login IP address must be a public IP address or IP address segment.
      -  Only one IP address can be added at a time. To add multiple IP addresses, repeat the operations until all IP addresses are added. Up to 20 IP addresses can be added.


   .. figure:: /_static/images/en-us_image_0000001862551820.png
      :alt: **Figure 4** Entering a common login IP address

      **Figure 4** Entering a common login IP address

5. Return to the **Security Configuration** tab of the **Installation & Configuration** page. Check whether the added locations are displayed on the **Common Login IP Addresses** subtab.

Configuring an SSH Login IP Address Whitelist
---------------------------------------------

The SSH login whitelist controls SSH access to servers to prevent account cracking.

.. note::

   -  An account can have up to 10 SSH login IP addresses in the whitelist.
   -  After you configure an SSH login IP address whitelist, SSH logins will be allowed only from whitelisted IP addresses.

      -  Before enabling this function, ensure that all IP addresses that need to initiate SSH logins are added to the whitelist. Otherwise, you cannot remotely log in to your server using SSH.

         If your service needs to access a server, but not necessarily via SSH, you do not need to add its IP address to the whitelist.

      -  Exercise caution when adding an IP address to the whitelist. This will make HSS no longer restrict access from this IP address to your servers.

#. Log in to the management console.

#. Click |image3| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. Choose **Installation & Configuration** and click the **Security Configuration** tab. Click **SSH IP Whitelist** and click **Add IP Address**.


   .. figure:: /_static/images/en-us_image_0000002051395986.png
      :alt: **Figure 5** Adding an IP address whitelist item

      **Figure 5** Adding an IP address whitelist item

4. In the dialog box that is displayed, enter an IP address and select servers. Confirm the information and click **OK**.

   .. note::

      -  A common login IP address must be a public IP address or IP address segment. Otherwise, you cannot remotely log in to the server in SSH mode.
      -  Only one IP address can be added at a time. To add multiple IP addresses, repeat the operations until all IP addresses are added.


   .. figure:: /_static/images/en-us_image_0000001862392004.png
      :alt: **Figure 6** Entering an IP address

      **Figure 6** Entering an IP address

5. Return to the **Security Configuration** tab of the **Installation & Configuration** page. Check whether the added locations are displayed on the **Common Login IP Addresses** subtab.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png
.. |image2| image:: /_static/images/en-us_image_0000001517477398.png
.. |image3| image:: /_static/images/en-us_image_0000001517477398.png

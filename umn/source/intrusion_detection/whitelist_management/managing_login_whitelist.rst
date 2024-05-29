:original_name: hss_01_0029.html

.. _hss_01_0029:

Managing Login Whitelist
========================

You can configure the IP addresses of destination servers, login IP addresses, login usernames, and user behaviors in the Login Whitelist.

.. note::

   -  If the destination server IP address, login IP address, and username of a login are all whitelisted, this login will be allowed without checking.
   -  After an IP address is added to a whitelist by following the instructions in :ref:`Adding Login Whitelist <hss_01_0029__section349913102296>`, the alarms (if any) that have been generated for the IP address will not be automatically cleared. Handle the alarms by referring to :ref:`Viewing Server Alarms <hss_01_0026>`.

You can add Login Whitelist in either of the following ways:

-  Add it to the Login Whitelist when handling false alarms of the **Brute-force attack** and **Abnormal login** types. For details, see :ref:`Viewing Server Alarms <hss_01_0026>`.
-  On the Login Whitelist page, add Login Whitelist.

.. _hss_01_0029__section349913102296:

Adding Login Whitelist
----------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

#. Choose **Detection** > **Whitelists** > **Login Whitelist** to access the **Whitelists** page, and click **Add**.


   .. figure:: /_static/images/en-us_image_0000001621634874.png
      :alt: **Figure 1** Adding Login Whitelist

      **Figure 1** Adding Login Whitelist

#. On the displayed page, enter the server IP address, login IP address, and login username.

   .. table:: **Table 1** Login security whitelist parameters

      +-----------------------+--------------------------------------------------------------------------------------------------------+----------------------------+
      | Parameter             | Description                                                                                            | Example Value              |
      +=======================+========================================================================================================+============================+
      | Server IP Address     | -  IPv4 addresses are supported                                                                        | -  192.168.1.1             |
      |                       | -  Single IP addresses, IP address segments, and masks are supported. Use commas (,) to separate them. | -  192.168.2.1-192.168.6.1 |
      |                       |                                                                                                        | -  192.168.7.0/24          |
      +-----------------------+--------------------------------------------------------------------------------------------------------+----------------------------+
      | Login IP Address      |                                                                                                        |                            |
      +-----------------------+--------------------------------------------------------------------------------------------------------+----------------------------+
      | Login Username        | Current login username                                                                                 | hss_test                   |
      +-----------------------+--------------------------------------------------------------------------------------------------------+----------------------------+
      | Remarks               | Custom whitelist description                                                                           | Test                       |
      +-----------------------+--------------------------------------------------------------------------------------------------------+----------------------------+

#. Click **OK**.

Other Operations
----------------

Removing Login Whitelist

To delete a Login Whitelist, select the Login Whitelist to you want to delete and click **Delete**, or click **Delete** in the **Operation** column of the server IP address you want to delete in the Login Whitelist.

.. note::

   Exercise caution when performing the deletion operation because it cannot be rolled back.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

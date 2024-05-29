:original_name: hss_01_0103.html

.. _hss_01_0103:

How Do I Enable Logging for Login Failures?
===========================================

MySQL
-----

The account hacking prevention function for Linux supports MySQL 5.6 and 5.7. Perform the following steps to enable logging for login failure:

#. Log in to the host as the **root** user.

#. Run the following command to query the **log_warnings** value:

   **show global variables like 'log_warnings**'

#. Run the following command to change the **log_warnings** value:

   **set global log_warnings=2**

#. Modify the configuration file.

   -  For a Linux OS, modify the **my.conf** file by adding **log_warnings=2** to **[MySQLd]**.

vsftp
-----

This section shows you how to enable logging for vsftp login failures.

#. Modify the configuration file (for example, **/etc/vsftpd.conf**) and set the following parameters:

   **vsftpd_log_file=log/file/path**

   **dual_log_enable=YES**

#. Restart the vsftp service. If the setting is successful, log records shown in the logs shown in :ref:`Figure 1 <hss_01_0103__fig167291123485>` will be returned when you log in to vsftp.

   .. _hss_01_0103__fig167291123485:

   .. figure:: /_static/images/en-us_image_0000001568517685.png
      :alt: **Figure 1** Log Records

      **Figure 1** Log Records

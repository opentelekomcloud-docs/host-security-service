:original_name: hss_01_0192.html

.. _hss_01_0192:

How Do I Know Whether an Intrusion Succeeded?
=============================================

-  If you have enabled alarm notifications for intrusion detection, you will be notified immediately when an account is cracked or may be cracked.
-  You can also check whether attack IP addresses are blocked on the **Detection** page.
-  To further determine the details, perform the following steps:

   -  Linux

      For Linux servers, you can view logs in **/var/log/secure** and **/var/log/message** directories, or run the **last** command to check whether there are abnormal login records.

   -  Windows

      To view server login logs, perform the following steps:

      #. Open **Control Panel**.
      #. Choose **Administrative Tools** > **Event Viewer**. The **Event Viewer** page is displayed.
      #. In the navigation tree on the left, choose **Windows Logs** > **Security**. The **Security** page is displayed.
      #. In the navigation tree on the right, choose **Security** > **Filter Current Log**. The **Filter Current Log** dialog box is displayed.
      #. On the **Filter** tab, locate the **<All Event IDs>**.
      #. Enter the login event ID and click **OK** to filter the target login events.

         -  4624: ID of successful login events
         -  4625: ID of failed login events

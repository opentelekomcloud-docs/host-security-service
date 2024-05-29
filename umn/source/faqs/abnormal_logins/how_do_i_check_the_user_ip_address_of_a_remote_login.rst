:original_name: hss_01_0091.html

.. _hss_01_0091:

How Do I Check the User IP address of a Remote Login?
=====================================================

Alarm Policies
--------------

The remote login detection function checks for remote logins into your servers in real time. HSS generates an alarm if it detects logins from locations other than the common login locations you set.

Viewing Remote Login Records on the Console
-------------------------------------------

#. Log in to the management console.
#. In the navigation pane on the left, choose **Detection** > **Alarms**, and click **Server Alarms**.
#. In the **Event Types** area, Choose **Abnormal User Behavior** > **Abnormal logins**, and click **Remote Login**.

Locally Viewing Remote Login Records
------------------------------------

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

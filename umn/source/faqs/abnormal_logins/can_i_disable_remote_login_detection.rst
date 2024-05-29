:original_name: hss_01_0120.html

.. _hss_01_0120:

Can I Disable Remote Login Detection?
=====================================

No.

If you do not want to receive remote login alarm notifications, add alarmed locations as common login locations, or deselect the remote login attempt item in alarm notification settings.

-  On the **Common Login Locations** tab, click **Add Common Login Location**, and add common login locations. HSS does not trigger remote login alarms on logins from common login locations.

-  Choose **Installation & Configuration** and click **Alarm Notifications**. In the **Masked Events** box, select **Abnormal logins**.

   Exercise caution when you deselect the **Abnormal Logins** notification item. Abnormal logins include remote logins and successful hacks. If you deselect this item, you will not receive alarms on brute-force attacks in real time.

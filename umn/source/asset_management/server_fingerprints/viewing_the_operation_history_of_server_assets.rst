:original_name: hss_01_0384.html

.. _hss_01_0384:

Viewing the Operation History of Server Assets
==============================================

HSS proactively records the changes on account information, software information, and auto-started items. You can check the change details according to different dimensions and time ranges.

Prerequisite
------------

HSS enterprise edition, premium edition, WTP edition, or container edition has been enabled for the server.

Checking Change Records
-----------------------

#. Log in to the management console.
#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.
#. Choose **Asset Management** > **Server Fingerprints** and click **Operation History**. On the displayed **Operation History** page, select a dimension and time period to view the change history of accounts, software, and auto-started items.

Managing Account Information
----------------------------

Account changes are recorded.

-  **Action**: The **Action** column records the operations. Its value can be **Create** (newly found in the latest check), **Delete** (found in earlier checks but missing in the latest check), and **Modify** (changes on account information, such as account names, administrator rights, and user groups, are detected).
-  **Last Scan Time**: The last scan time indicates the time of the latest scan performed for servers in a period.

You can check the information about and changes on all accounts here. If you find unnecessary or super-privileged accounts (such as **root**) that are not mandatory for services, delete them or modify their permissions to prevent exploits.

Managing Software
-----------------

Operations made to accounts are recorded.

-  **Action**: **Create** and **Delete**.
-  **Last Scan Time**: The last scan time records the time when the changes were detected, not the time they were made.

You can check the information about and changes on all software, upgrade software, and delete software that is unnecessary, suspicious, or in old version.

Auto-started Items
------------------

Trojans usually intrude servers by creating auto-started services, scheduled tasks, preloaded dynamic libraries, run registry keys, or startup folders. The auto-startup check function collects information about all auto-started items, including their names, types, and number of affected servers, making it easy for you to locate suspicious auto-started items.

You can check the servers, IP addresses, changes, paths, file hashes, users, and last scan time of auto-startup items.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

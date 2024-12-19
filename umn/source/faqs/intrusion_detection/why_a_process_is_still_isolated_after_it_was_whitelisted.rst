:original_name: hss_01_0207.html

.. _hss_01_0207:

Why a Process Is Still Isolated After It Was Whitelisted?
=========================================================

After you add a process to the whitelist, it will no longer trigger certain alarms, but its isolation will not be automatically canceled. If your process is isolated, you need to manually restore it.

Isolating and Killing a Malicious Program
-----------------------------------------

-  Choose **Installation & Configuration** and click the **Security Configuration** tab. Click the **Isolation and Killing of Malicious Programs** tab and enable this function.
-  Choose **Intrusion Detection** > **Alarms**. In the **Events** area, manually isolate and kill malicious programs.

If a program is isolated and killed, it will be terminated immediately and no longer able to perform read or write operations. Isolated source files of programs or processes are displayed on the **Isolated Files** slide-out panel and cannot harm your servers.

Canceling the Isolation of Files
--------------------------------

#. Choose **Intrusion Detection** > **Alarms**. Click the value above **Isolated Files** to view the isolated files.

#. In the row containing the target server, click **Restore** in the **Operation** column. The dialog box is displayed.

#. Click **OK** to restore the isolation file.

   After you cancel isolation, the read/write permissions of files will be restored, but terminated processes will not be automatically started.

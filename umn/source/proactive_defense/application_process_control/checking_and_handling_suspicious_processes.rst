:original_name: hss_01_0535.html

.. _hss_01_0535:

Checking and Handling Suspicious Processes
==========================================

If HSS detects suspicious processes on servers, the processes will be displayed in the suspicious process list but will not trigger alarms. HSS cannot determine whether these processes are trustworthy based on the application process characteristics. To avoid affecting services, you need to check whether the processes can be trusted and add trustworthy ones to the process whitelist.


Checking and Handling Suspicious Processes
------------------------------------------

#. Log in to the management console.

2. In the navigation tree, choose **Prevention** > **Application Process Control**.

3. Click the **Suspicious Processes** tab.

4. Determine whether a suspicious process is malicious based on its information, such as the hash value and file path.

5. In the row of a process, click **Handle** in the **Operation** column.

   You can also select multiple suspicious processes and click **Batch Handle** above the list.

6. In the dialog box that is displayed, select an action.

   Select **Add to process whitelist**.

7. Click **OK**.

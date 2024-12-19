:original_name: hss_01_0504.html

.. _hss_01_0504:

What Do I Do If Self-Protection Cannot Be Disabled?
===================================================

Root Causes
-----------

If the server network is disconnected, agents cannot receive the command for disabling self-protection delivered by the HSS console. Therefore, HSS self-protection cannot be disabled.

Solutions
---------

#. .

#. In the navigation pane on the left, choose **Asset Management** > **Servers & Quota**.

#. Click the **Servers** tab, click |image1| in the upper right corner of the server list and select **Agent ID**.

#. Above the server list, enter a server name or ID and click |image2| to search for the Windows server for which you want to disable the HSS self-protection.

#. In the row of the target Windows server, copy the first eight characters from the **Agent ID** column.

#. Run **cmd** as the administrator.

#. Run the following command to disable HSS self-protection:

   **"C:\\Program Files\\HostGuard\\bin\\HssClient.exe"1234abcd**

   .. note::

      **1234abcd** in the command indicates the first eight characters of the agent ID. The first eight characters of the agent ID are used as the verification code when **HSSClient.exe** is executed. It is to prevent malicious programs from disabling self-protection and user misoperations. Self-protection can be disabled only when the first eight characters of the agent ID are correct.

#. If **Disable self protect succeed.** is displayed, HSS self-protection is disabled successfully.

.. |image1| image:: /_static/images/en-us_image_0000001630979629.png
.. |image2| image:: /_static/images/en-us_image_0000001580861324.png

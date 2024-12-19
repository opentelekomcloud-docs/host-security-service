:original_name: hss_01_0567.html

.. _hss_01_0567:

Isolating and Killing Malicious Programs
========================================

HSS automatically isolates and kills identified malicious programs, such as web shells, Trojans, and worms, removing security risks.


Isolating and Killing Malicious Programs
----------------------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. Choose **Installation & Configuration** and click the **Security Configuration** tab.Click the **Isolation and Killing of Malicious Programs** tab and enable **Isolate and Kill Malicious Programs**.

   .. note::

      After the cloud scan function is enabled, all HSS servers will be scanned. Some HSS quota editions can support only limited scanning capabilities. Therefore, you are advised to enable the enterprise edition or higher to enjoy all capabilities of the isolation and killing function.


   .. figure:: /_static/images/en-us_image_0000002087556837.png
      :alt: **Figure 1** Enabling isolation and killing

      **Figure 1** Enabling isolation and killing

4. In the confirmation dialog box, click **OK** to enable the isolation and killing of malicious programs.

   Automatic isolation and killing may cause false positives. You can choose **Intrusion Detection** > **Events** to view isolated malicious programs. You can cancel the isolation or ignore misreported malicious programs.

   .. important::

      -  When a program is isolated and killed, the process of the program is terminated immediately. To avoid impact on services, check the detection result, and cancel the isolation of or unignore misreported malicious programs (if any).

      -  If **Isolate and Kill Malicious Programs** is set to **Disable** on the **Isolation and Killing of Malicious Programs** tab, HSS will generate an alarm when it detects a malicious program.

         To isolate and kill the malicious programs that triggered alarms, choose **Intrusion Detection** > **Events** and click **Malicious program**.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

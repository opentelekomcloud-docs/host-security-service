:original_name: hss_01_0202.html

.. _hss_01_0202:

What Should I Do If WTP Cannot Be Enabled?
==========================================

The causes of this problem vary by scenarios.

Agent Status Is Abnormal
------------------------

-  **Symptom**

   The agent status is **Offline** or **Not installed** in the server list on the **Web Tamper Protection** page.

-  **Solution**

   Rectify the fault by following the instructions provided in *How Do I Fix an Abnormal Agent*. Ensure that **Agent Status** in the server list is **Online**.

Enterprise/Premium Edition HSS Has Been Enabled
-----------------------------------------------

-  **Symptom**

   **Protection Status** is **Enabled** in the server list on the HSS console.

-  **Solution**

   Disable HSS and then enable WTP.

   .. note::

      HSS editions include the enterprise, premium, and WTP editions. Before enabling WTP for a server, ensure that enterprise, or premium edition HSS has been disabled for the server.

Protection Was Enabled on the Wrong Page
----------------------------------------

To enable WTP, choose **Web Tamper Protection** > **Servers**.

.. note::

   If you have applied for the WTP edition, you can use all functions of the premium edition, and you can enable the server protection only on the **Web Tamper Protection**. After WTP is enabled, server protection of the premium edition is also enabled.

:original_name: hss_01_0563.html

.. _hss_01_0563:

Extending the Process Whitelist
===============================

After HSS completes learning on the servers associated a policy, if you find the learning outcomes are much fewer than the process fingerprints detected by HSS, or if too many suspicious processes are reported, you can extend the whitelist. HSS will compare the application processes it learned with and the asset fingerprints it detected, identify trustworthy processes, and add them to the process whitelist.


Extending the Process Whitelist
-------------------------------

#. Log in to the management console.

2. In the navigation tree, choose **Prevention** > **Application Process Control**.

3. Click the **Whitelist Policies** tab.
4. Click a policy name. The **Policy Details** page is displayed.
5. Click the **Associated Servers** tab.
6. In the row of a server, choose **More** > **Add to Whitelist** in the **Operation** column.
7. Click **Compare** to compare the server process fingerprint with the application processes learned by HSS.
8. Select trustworthy processes and click **Add**.

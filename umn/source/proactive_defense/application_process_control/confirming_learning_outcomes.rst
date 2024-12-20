:original_name: hss_01_0533.html

.. _hss_01_0533:

Confirming Learning Outcomes
============================

After HSS completes learning on the servers associated with a whitelist policy, there may be some suspicious processes with insignificant characteristics that need to be confirmed. You can manually or let HSS automatically mark them as suspicious, malicious, or trustworthy processes.

You can configure how to confirm learning outcomes when creating a whitelist policy. The value of **Confirm Learning Outcomes** can be:

-  **Automatically**: Suspicious processes are automatically marked based on the application process intelligence.
-  **Manually**: You need to manually check and mark suspicious processes. This section describes the detailed procedure.

Prerequisites
-------------

A policy has been created and its status is **Learning complete but not in effect**. For details, see :ref:`Creating a Whitelist Policy <hss_01_0532>`.


Confirming Learning Outcomes
----------------------------

#. Log in to the management console.

2. In the navigation tree, choose **Prevention** > **Application Process Control**.
3. Click the **Whitelist Policies** tab.
4. Click the name of a policy whose **Policy Status** is **Learning complete but not in effect**. The **Policy Details** page is displayed.
5. Click the **Process Files** tab.
6. Click the number of processes to be confirmed.

7.  Check whether the application processes are trustworthy based on their names and file paths.

8.  In the row of a process, click **Mark** in the **Operation** column.

    You can also select all application processes and click **Batch Mark** above the process list.

9.  In the **Mark** dialog box, set **Trust Status**.

    Select **Suspicious**, **Trusted**, or **Malicious**.

10. Click **OK**.

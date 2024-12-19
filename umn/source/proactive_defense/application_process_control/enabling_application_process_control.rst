:original_name: hss_01_0534.html

.. _hss_01_0534:

Enabling Application Process Control
====================================

HSS can control different types of application processes on servers. Suspicious and trusted processes are allowed to run, and alarms are generated for malicious processes.

You can configure how to enable application process control when creating a whitelist policy. The value of **Apply Policy After Learning** can be:

-  **Automatically**: Application process control is automatically enabled after HSS completes learning on the servers associated with the policy.
-  **Manually**: Manually enable application process control as needed after HSS completes learning. This section describes the detailed procedure.

Prerequisites
-------------

A whitelist policy has been created and the policy learning outcomes have been confirmed. For details, see :ref:`Creating a Whitelist Policy <hss_01_0532>` and :ref:`Confirming Learning Outcomes <hss_01_0533>`.


Enabling Application Process Control
------------------------------------

#. Log in to the management console.

2. In the navigation tree, choose **Prevention** > **Application Process Control**.

3. Click the **Whitelist Policies** tab.

4. In the **Operation** column of a policy, click **Enable Protection**.

   You can also select multiple policies and click **Enable Protection** above the policy list.

5. In the **Enable Protection** dialog box, click **OK**.

6. Check the policy status. If **Policy Status** is **Learning complete and in effect**, application protection has been enabled.

:original_name: hss_01_0542.html

.. _hss_01_0542:

Disabling Application Process Control
=====================================

You can disable application process control for one or multiple servers at a time.

Disabling Protection for Servers Associated with a Policy
---------------------------------------------------------

#. Log in to the management console.

2. In the navigation tree, choose **Prevention** > **Application Process Control**.

3. Click the **Whitelist Policies** tab.
4. Disable application process control.

   -  Disable protection but retain the application process characteristics learned by HSS.

      a. In the **Operation** column of a policy, click **Disable Protection**. Alternatively, select multiple policies and click **Disable** above the policy list.
      b. Click **OK**.

   -  Disable protection and delete the application process characteristics learned by HSS.

      a. In the row of a policy, click **Delete** in the **Operation** column.
      b. Click **OK**.

5. Check the policy list.

   -  Disable protection but retain the application process characteristics learned by HSS.

      If the **Policy Status** of the policy is **Learning complete but not in effect**, application process control has been disabled.

   -  Disable protection and delete the application process characteristics learned by HSS.

      If the policy is deleted from the policy list, application process control has been disabled.

Disabling Protection for a Single Server
----------------------------------------

#. Log in to the management console.

2. In the navigation tree, choose **Prevention** > **Application Process Control**.

3. Click the **Whitelist Policies** tab.
4. Click a policy name. The **Policy Details** page is displayed.
5. Click the **Associated Servers** tab.
6. Disable application process control.

   -  Disable protection but retain the association between the server and the policy.

      a. In the **Operation** column of a policy, click **Disable Protection**. Alternatively, select multiple policies and click **Disable** above the policy list.
      b. Click **OK**.

   -  Disable protection and disassociate the server from the policy.

      .. note::

         To change the protection policy associated with a server, remove the server from the policy settings, and then create or edit another protection policy to associate with the server.

      a. In the row containing the desired instance, click **Delete** in the **Operation** column.
      b. Click **OK**.

7. Check the server list.

   -  Disable protection but retain the association between the server and the policy.

      If the **Policy Status** of the server is **Learning complete but not in effect**, application process control has been disabled.

   -  Disable protection and disassociate the server from the policy.

      If the server is deleted from the list, application process control has been disabled.

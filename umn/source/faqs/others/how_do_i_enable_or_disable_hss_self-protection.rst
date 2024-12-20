:original_name: hss_01_0511.html

.. _hss_01_0511:

How Do I Enable or Disable HSS Self-protection?
===============================================

HSS self-protection protect HSS files, processes, and software from malicious programs, which may uninstall HSS agents, tamper with HSS files, or stop HSS processes.

Constraints
-----------

-  HSS self-protection is supported only for Windows servers that enabled HSS premium or WTP edition.
-  Self-protection in Windows depends on antivirus detection, HIPS detection, and ransomware protection. It takes effect only when more than one of the three functions are enabled. For more details, see:

   -  .
   -  Antivirus detection and HIPS detection are enabled by default. If you manually disable the two detection items, enable them again by referring to .

-  Enabling the self-protection policy has the following impacts:

   -  The agent cannot be uninstalled on the control panel of a Windows server. It can be uninstalled on the HSS console.
   -  In the agent installation path **C:\\Program Files\\HostGuard**, you can only access the **log** and **data** directories (and the **upgrade** directory, if your agent has been upgraded).
   -  Hide the process information of HSS.

Procedure
---------

#. Log in to the management console.

#. In the navigation tree on the left, choose **Security Operations** > **Policies**

#. Click the name of a premium edition policy group for Windows servers. The policy group details page is displayed.

   Select the policy group of the server where you want to enable self-protection.

   -  If you have not created any policy groups of premium edition, you can select the default policy group of the premium or WTP edition. The group name format is **tenant**\ *\_XXX_XXX*\ **\_default_policy_group**.
   -  If you have created policy groups of premium edition, select the policy group of your server. Perform the following operations:

      a. In the navigation tree on the left, choose **Asset Management** > **Servers & Quota**.
      b. Click the **Servers** tab to view the policy groups of servers.

#. In the row containing the target self-protection policy, click **Enable** or **Disable** in the **Operation** column.

#. In the displayed dialog box, click **OK**.

Related Operations
------------------

**Disabling HSS Self-Protection**

#. In the row containing the target self-protection policy, click **Disable** in the **Operation** column.
#. In the displayed dialog box, click **OK**.

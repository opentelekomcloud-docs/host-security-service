:original_name: hss_01_0095.html

.. _hss_01_0095:

How Do I Set a Proper Password Complexity Policy in a Windows OS?
=================================================================

A proper password complexity policy would be: eight characters for the length of a password and at least three types of the following characters used: uppercase letters, lowercase letters, digits, and special characters.

Perform the following steps to set a local security policy:

#. Log in to the OS as user **Administrator**. Choose **Start** > **Control Panel** > **System and Security** > **Administrative Tools**. In the **Administrative Tools** folder, double-click **Local Security Policy**.

   .. note::

      -  Alternatively, click **Start** and type **secpol.msc** in the **Search programs and files** box.
      -  When a policy is applied to a server, the domain policy takes precedence over the locally defined policy on the server.

#. Choose **Account Policies** > **Password Policy** and perform the following operations.

   -  Double-click **Password must meet complexity requirements**, select **Enable**, and click **OK** to enable the policy.
   -  Double-click **Minimum password length**, enter the length (greater than or equal to **8**), and click **OK** to set the policy.

#. Press **Windows**\ +\ **R** to open the **Run** window.

#. Enter **cmd** and click **OK**. The command prompt window is displayed.

#. Run the following command to refresh policies:

   **gpupdate/force**

   After the refreshing, the settings will be applied.

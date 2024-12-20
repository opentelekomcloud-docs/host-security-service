:original_name: hss_01_0206.html

.. _hss_01_0206:

What Do I Do If My Servers Are Subjected to a Mining Attack?
============================================================

Take immediate measures to contain the attack, preventing miners from occupying CPU or affecting other applications. If a server is intruded by a mining program, the mining program may penetrate the intranet and persist on the intruded server.

You should also harden your servers to better block intrusions.

Troubleshooting Procedure
-------------------------

#. Log in to the management console.

#. Check **Abnormal process behavior** events.

   Choose **Intrusion Detection** > **Alarms** and click **Server Alarms**. Choose **Abnormal System Behavior** > **Abnormal process behavior** to view and handle the abnormal process behavior alarms. Click **Handle** in the **Operation** column of an event.

#. Check auto-startup items. Some of your auto-startup items were probably created by attackers to start mining programs upon server restart.

   Choose **Asset Management** > **Server Fingerprints**, click **Auto-startup**, and select **Operation History** to view the change history.

Hardening Servers
-----------------

After you delete miner programs, harden your servers to better defend against intrusions.

**Linux servers**

#. Let HSS automatically scan your servers and applications in the early morning every day to help you detect and eliminate security risks.
#. Set stronger passwords for all accounts (including system and application accounts), or change the login mode to key-based login.

   a. Set the security password. For details, see :ref:`How Do I Set a Secure Password? <hss_01_0166>`.
   b. Use the key to log in to the server.

#. Strictly control the usage of system administrator accounts. Grant only the least permissions required for applications and middleware and strictly control their usage.
#. Configure access rules in security groups. Open only necessary ports. For special ports (such as remote login ports), only allow access from specified IP addresses or use VPN or bastion hosts to establish your own communications channels.

**Windows servers**

Use HSS to comprehensively check for and eliminate security risks. Improve your account, password, and authorization security.

-  **Account hardening**

   +-----------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
   | Measure                                                   | Description                                                                                                                       | Procedure                                                                                      |
   +===========================================================+===================================================================================================================================+================================================================================================+
   | Ensure default account security.                          | -  Disable user **Guest**.                                                                                                        | #. Open **Control Panel**.                                                                     |
   |                                                           | -  Disable and delete unnecessary accounts. (You are advised to disable inactive accounts for three months before deleting them.) | #. Click **Administrative Tools**. Open **Computer Management**.                               |
   |                                                           |                                                                                                                                   | #. Choose **System Tools** > **Local Users and Groups** > **Users**.                           |
   |                                                           |                                                                                                                                   | #. Double-click **Guest**. In the **Guest Properties** window, select **Account is disabled**. |
   |                                                           |                                                                                                                                   | #. Click **OK**.                                                                               |
   +-----------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
   | Assign accounts with only necessary permissions to users. | Create users and user groups of specific types.                                                                                   | #. Open **Control Panel**.                                                                     |
   |                                                           |                                                                                                                                   | #. Click **Administrative Tools**. Open **Computer Management**.                               |
   |                                                           | Example: administrators, database users, audit users                                                                              | #. Choose **System Tools** > **Local Users and Groups**. Create users and groups as needed.    |
   +-----------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
   | Periodically check and delete unnecessary accounts.       | Periodically delete or lock unnecessary accounts.                                                                                 | #. Open **Control Panel**.                                                                     |
   |                                                           |                                                                                                                                   | #. Click **Administrative Tools**. Open **Computer Management**.                               |
   |                                                           |                                                                                                                                   | #. Choose **System Tools** > **Local Users and Groups**.                                       |
   |                                                           |                                                                                                                                   | #. Choose **Users** or **User Groups** and delete unnecessary users or user groups.            |
   +-----------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+
   | Do not display the last username.                         | Forbid the login page from displaying the latest logged in user.                                                                  | #. Open **Control Panel**.                                                                     |
   |                                                           |                                                                                                                                   | #. Click **Administrative Tools**. Open **Local Security Policy**.                             |
   |                                                           |                                                                                                                                   | #. Choose **Local Policies** > **Security Options**.                                           |
   |                                                           |                                                                                                                                   | #. Double-click **Interactive logon: Do not display last user name**.                          |
   |                                                           |                                                                                                                                   | #. In the displayed dialog box, select **Enable** and click **OK**.                            |
   +-----------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------------+

-  **Password hardening**

   +------------------------+----------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------+
   | Setting                | Description                                                                                                                | Procedure                                                            |
   +========================+============================================================================================================================+======================================================================+
   | Complexity             | In line with the requirements set in :ref:`How Do I Set a Secure Password <hss_01_0166>`.                                  | #. Open **Control Panel**.                                           |
   |                        |                                                                                                                            | #. Click **Administrative Tools**. Open **Local Security Policy**.   |
   |                        |                                                                                                                            | #. Choose **Account Policies** > **Password Policy**.                |
   |                        |                                                                                                                            | #. Enable the policy **Password must meet complexity requirements**. |
   +------------------------+----------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------+
   | Maximum password age   | In static password authentication mode, force users to change their passwords every 90 days or at shorter intervals.       | #. Open **Control Panel**.                                           |
   |                        |                                                                                                                            | #. Click **Administrative Tools**. Open **Local Security Policy**.   |
   |                        |                                                                                                                            | #. Choose **Account Policies** > **Password Policy**.                |
   |                        |                                                                                                                            | #. Set **Maximum password age** to 90 days or shorter.               |
   +------------------------+----------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------+
   | Account lockout policy | In static password authentication mode, lock a user account if authentication for the user fails for 10 consecutive times. | #. Open **Control Panel**.                                           |
   |                        |                                                                                                                            | #. Click **Administrative Tools**. Open **Local Security Policy**.   |
   |                        |                                                                                                                            | #. Choose **Account Policies** > **Account Lockout Policy**.         |
   |                        |                                                                                                                            | #. Set **Account lockout threshold** to **10** or smaller.           |
   +------------------------+----------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------+

-  **Authorization hardening**

   +-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------------------------------------------------------------------------+
   | Authorization           | Description                                                                                                                                              | Procedure                                                                                              |
   +=========================+==========================================================================================================================================================+========================================================================================================+
   | Remote shutdowns        | Assign the permission **Force shutdown from a remote system** only to the **Administrators** group.                                                      | #. Open **Control Panel**.                                                                             |
   |                         |                                                                                                                                                          | #. Click **Administrative Tools**. Open **Local Security Policy**.                                     |
   |                         |                                                                                                                                                          | #. Choose **Local Policies** > **User Rights Assignment**.                                             |
   |                         |                                                                                                                                                          | #. Assign the permission **Force shutdown from a remote system** only to the **Administrators** group. |
   +-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------------------------------------------------------------------------+
   | Local shutdown          | Assign the permission **Shut down the system** only to the **Administrators** group.                                                                     | #. Open **Control Panel**.                                                                             |
   |                         |                                                                                                                                                          | #. Click **Administrative Tools**. Open **Local Security Policy**.                                     |
   |                         |                                                                                                                                                          | #. Choose **Local Policies** > **User Rights Assignment**.                                             |
   |                         |                                                                                                                                                          | #. Assign the permission **Shut down the system** only to the **Administrators** group.                |
   +-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------------------------------------------------------------------------+
   | User rights assignment  | Assign the permission **Take ownership of files or other objects** only to the **Administrators** group.                                                 | #. Open **Control Panel**.                                                                             |
   |                         |                                                                                                                                                          | #. Click **Administrative Tools**. Open **Local Security Policy**.                                     |
   |                         |                                                                                                                                                          | #. Choose **Local Policies** > **User Rights Assignment**.                                             |
   |                         |                                                                                                                                                          | #. Assign the permission **Shut down the system** only to the **Administrators** group.                |
   +-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------------------------------------------------------------------------+
   | Login                   | Authorize users to log in to the computer locally.                                                                                                       | #. Open **Control Panel**.                                                                             |
   |                         |                                                                                                                                                          | #. Click **Administrative Tools**. Open **Local Security Policy**.                                     |
   |                         |                                                                                                                                                          | #. Choose **Local Policies** > **User Rights Assignment**.                                             |
   |                         |                                                                                                                                                          | #. Assign the permission **Allow log on locally** to the users you want to authorize.                  |
   +-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------------------------------------------------------------------------+
   | Access from the network | Allow only the authorized users to access this computer from the network (for example, by network sharing). Access from other terminals are not allowed. | #. Open **Control Panel**.                                                                             |
   |                         |                                                                                                                                                          | #. Click **Administrative Tools**. Open **Local Security Policy**.                                     |
   |                         |                                                                                                                                                          | #. Choose **Local Policies** > **User Rights Assignment**.                                             |
   |                         |                                                                                                                                                          | #. Assign the permission **Access this computer from the network** to the users you want to authorize. |
   +-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------------------------------------------------------------------------+

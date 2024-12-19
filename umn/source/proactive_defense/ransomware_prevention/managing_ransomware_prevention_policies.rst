:original_name: hss_01_0349.html

.. _hss_01_0349:

Managing Ransomware Prevention Policies
=======================================

You can use predefined policies, modify ransomware prevention policies, or change the policy associated with a server.

.. important::

   Currently, you can create a ransomware prevention policy only when enabling ransomware prevention.

Constraints
-----------

Only premium, WTP, and container editions support ransomware protection.

Changing a Policy
-----------------

You can change the protection policy associated with a server.

#. Log in to the management console.
#. Choose **Prevention** > **Ransomware Prevention**.
#. Click the **Protected Servers** tab.
#. Select a server and click **Change Policy**.
#. In the **Change Policy** dialog box, select a protection policy.
#. Click **OK**.

Modifying a Policy
------------------

#. Log in to the management console and go to the HSS page.

#. In the navigation pane, choose **Prevention** > **Ransomware Prevention**. Click the **Policies** tab.

#. Click **Edit** in the **Operation** column of a policy. Edit the policy configurations and associated servers. For more information, see :ref:`Table 1 <hss_01_0349__table1194918551568>`.

   The following uses a Linux server as an example. On the **Protected Servers** tab, you can also click the name of the policy associated with the server to edit the policy.

   .. _hss_01_0349__table1194918551568:

   .. table:: **Table 1** Protection policy parameters

      +-------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------+
      | Parameter                     | Description                                                                                                                                                                                                                                                                                                            | Example Value              |
      +===============================+========================================================================================================================================================================================================================================================================================================================+============================+
      | Policy                        | Policy name.                                                                                                                                                                                                                                                                                                           | test                       |
      +-------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------+
      | Action                        | How an event is handled.                                                                                                                                                                                                                                                                                               | Report alarm and isolate   |
      |                               |                                                                                                                                                                                                                                                                                                                        |                            |
      |                               | -  **Report alarm and isolate**                                                                                                                                                                                                                                                                                        |                            |
      |                               | -  **Report alarm**                                                                                                                                                                                                                                                                                                    |                            |
      +-------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------+
      | Dynamic Honeypot Protection   | After bait protection is enabled, the system deploys bait files in protected directories and other random positions (unless otherwise specified by users). A bait file occupies a few server resources. Therefore, configure the directories that you do not want to deploy the bait file in the excluded directories. | Enabled                    |
      |                               |                                                                                                                                                                                                                                                                                                                        |                            |
      |                               | .. note::                                                                                                                                                                                                                                                                                                              |                            |
      |                               |                                                                                                                                                                                                                                                                                                                        |                            |
      |                               |    Currently, Linux servers support dynamic generation and deployment of bait files. Windows servers support only static deployment of bait files.                                                                                                                                                                     |                            |
      +-------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------+
      | Bait File Directories         | Directory that needs to be protected by static bait (excluding subdirectories). You are advised to configure important service directories or data directories.                                                                                                                                                        | Linux: **/etc**            |
      |                               |                                                                                                                                                                                                                                                                                                                        |                            |
      |                               | Separate multiple directories with semicolons (;). You can configure up to 20 directories.                                                                                                                                                                                                                             | Windows: **C:\\Test**      |
      |                               |                                                                                                                                                                                                                                                                                                                        |                            |
      |                               | This parameter is mandatory for Linux servers and optional for Windows servers.                                                                                                                                                                                                                                        |                            |
      +-------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------+
      | Excluded Directory (Optional) | Directory that does not need to be protected by bait files.                                                                                                                                                                                                                                                            | Linux: **/etc/lesuo**      |
      |                               |                                                                                                                                                                                                                                                                                                                        |                            |
      |                               | Separate multiple directories with semicolons (;). You can configure up to 20 excluded directories.                                                                                                                                                                                                                    | Windows: C:\\Test\\ProData |
      +-------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------+
      | Protected File Type           | Types of files to be protected.                                                                                                                                                                                                                                                                                        | Select all                 |
      |                               |                                                                                                                                                                                                                                                                                                                        |                            |
      |                               | More than 70 file formats can be protected, including databases, containers, code, certificate keys, and backups.                                                                                                                                                                                                      |                            |
      |                               |                                                                                                                                                                                                                                                                                                                        |                            |
      |                               | This parameter is mandatory for Linux servers only.                                                                                                                                                                                                                                                                    |                            |
      +-------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------+
      | Associate Servers             | Information about the server associated with the policy. If you want to disassociate the server (disable ransomware protection), you can delete the policy.                                                                                                                                                            | ``-``                      |
      +-------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------+

#. Confirm the policy information and click **OK**.

Deleting a Policy
-----------------

#. Log in to the management console and go to the HSS page.
#. In the navigation pane, choose **Prevention** > **Ransomware Prevention**. Click the **Policies** tab.
#. Click **Delete** in the **Operation** column of the target policy.

   .. note::

      After a policy is deleted, the associated servers are no longer protected. Before deleting a policy, you are advised to bind its associated servers to other policies.

#. Confirm the policy information and click **OK**.

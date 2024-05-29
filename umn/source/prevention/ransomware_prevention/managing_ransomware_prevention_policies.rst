:original_name: hss_01_0349.html

.. _hss_01_0349:

Managing Ransomware Prevention Policies
=======================================

.. important::

   Currently, you can create a ransomware prevention policy only when enabling ransomware prevention.

Constraints
-----------

Only premium, WTP, and container editions support ransomware protection.

Creating a Policy
-----------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

#. In the navigation pane, choose **Prevention** > **Ransomware Prevention**. Click the **Protected Servers** tab. Click **Add Server**.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.

#. In the slide pane that is displayed, select **Linux** or **Windows**, enable protection, and select **Create new**. For more information, see :ref:`Table 1 <hss_01_0349__table4502192113419>`.

   The following uses a Linux server as an example.


   .. figure:: /_static/images/en-us_image_0000001621339160.png
      :alt: **Figure 1** Creating a policy

      **Figure 1** Creating a policy

   .. _hss_01_0349__table4502192113419:

   .. table:: **Table 1** Protection policy parameters

      +-------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------------+
      | Parameter                     | Description                                                                                                                                                                                                                                | Example Value                |
      +===============================+============================================================================================================================================================================================================================================+==============================+
      | Policy                        | Policy name                                                                                                                                                                                                                                | test                         |
      +-------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------------+
      | Action                        | Indicates how an event is handled.                                                                                                                                                                                                         | **Report alarm and isolate** |
      |                               |                                                                                                                                                                                                                                            |                              |
      |                               | -  **Report alarm and isolate**                                                                                                                                                                                                            |                              |
      |                               | -  **Report alarm**                                                                                                                                                                                                                        |                              |
      +-------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------------+
      | Bait File                     | After bait protection is enabled, the system deploys bait files in protected directories and key directories (unless otherwise specified by users). A bait file occupies only a few resources and does not affect your server performance. | Enabled                      |
      |                               |                                                                                                                                                                                                                                            |                              |
      |                               | If ransomware prevention is enabled, this function is enabled by default.                                                                                                                                                                  |                              |
      |                               |                                                                                                                                                                                                                                            |                              |
      |                               | .. note::                                                                                                                                                                                                                                  |                              |
      |                               |                                                                                                                                                                                                                                            |                              |
      |                               |    Currently, Linux servers support dynamic generation and deployment of bait files. Windows servers support only static deployment of bait files.                                                                                         |                              |
      +-------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------------+
      | Bait File Directories         | Protected directories (excluding subdirectories).                                                                                                                                                                                          | Linux: /etc/lesuo            |
      |                               |                                                                                                                                                                                                                                            |                              |
      |                               | Separate multiple directories with semicolons (;). You can configure up to 20 directories.                                                                                                                                                 | Windows: C:\\Test            |
      |                               |                                                                                                                                                                                                                                            |                              |
      |                               | This parameter is mandatory for Linux servers and optional for Windows servers.                                                                                                                                                            |                              |
      +-------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------------+
      | Excluded Directory (Optional) | Directories where bait files are not deployed.                                                                                                                                                                                             | Linux: /test                 |
      |                               |                                                                                                                                                                                                                                            |                              |
      |                               | Separate multiple directories with semicolons (;). You can configure up to 20 excluded directories.                                                                                                                                        | Windows: C:\\ProData         |
      +-------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------------+
      | Protected File Type           | Types of files to be protected.                                                                                                                                                                                                            | Select all                   |
      |                               |                                                                                                                                                                                                                                            |                              |
      |                               | More than 70 file formats can be protected, including databases, containers, code, certificate keys, and backups.                                                                                                                          |                              |
      |                               |                                                                                                                                                                                                                                            |                              |
      |                               | This parameter is mandatory for Linux servers only.                                                                                                                                                                                        |                              |
      +-------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------------+

#. Click **Next** and select servers. You can search for a server by its name or by filtering.


   .. figure:: /_static/images/en-us_image_0000001621219284.png
      :alt: **Figure 2** Selecting servers

      **Figure 2** Selecting servers

#. Click **OK** to enable ransomware protection and create the policy.

#. In the navigation pane, choose **Prevention** > **Ransomware Prevention**. Click the **Policies** tab and check the new policy.

Modifying a Policy
------------------

#. Log in to the management console and go to the HSS page.

#. In the navigation pane, choose **Prevention** > **Ransomware Prevention**. Click the **Policies** tab.

#. Click **Edit** in the **Operation** column of a policy. Edit the policy configurations and associated servers. For more information, see :ref:`Table 2 <hss_01_0349__table076204617243>`.

   The following uses a Linux server as an example. On the **Protected Servers** tab, you can also click the name of the policy associated with the server to edit the policy.

   .. _hss_01_0349__table076204617243:

   .. table:: **Table 2** Protection policy parameters

      +-------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------------+
      | Parameter                     | Description                                                                                                                                                                                                                                | Example Value                |
      +===============================+============================================================================================================================================================================================================================================+==============================+
      | Policy                        | Policy name                                                                                                                                                                                                                                | test                         |
      +-------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------------+
      | Action                        | Indicates how an event is handled.                                                                                                                                                                                                         | **Report alarm and isolate** |
      |                               |                                                                                                                                                                                                                                            |                              |
      |                               | -  **Report alarm and isolate**                                                                                                                                                                                                            |                              |
      |                               | -  **Report alarm**                                                                                                                                                                                                                        |                              |
      +-------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------------+
      | Bait File                     | After bait protection is enabled, the system deploys bait files in protected directories and key directories (unless otherwise specified by users). A bait file occupies only a few resources and does not affect your server performance. | Enabled                      |
      |                               |                                                                                                                                                                                                                                            |                              |
      |                               | If ransomware prevention is enabled, this function is enabled by default.                                                                                                                                                                  |                              |
      |                               |                                                                                                                                                                                                                                            |                              |
      |                               | .. note::                                                                                                                                                                                                                                  |                              |
      |                               |                                                                                                                                                                                                                                            |                              |
      |                               |    Currently, Linux servers support dynamic generation and deployment of bait files. Windows servers support only static deployment of bait files.                                                                                         |                              |
      +-------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------------+
      | Bait File Directories         | Protected directories (excluding subdirectories).                                                                                                                                                                                          | Linux: /etc/lesuo            |
      |                               |                                                                                                                                                                                                                                            |                              |
      |                               | Separate multiple directories with semicolons (;). You can configure up to 20 directories.                                                                                                                                                 | Windows: C:\\Test            |
      |                               |                                                                                                                                                                                                                                            |                              |
      |                               | This parameter is mandatory for Linux servers and optional for Windows servers.                                                                                                                                                            |                              |
      +-------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------------+
      | Excluded Directory (Optional) | Directories where bait files are not deployed.                                                                                                                                                                                             | Linux: /test                 |
      |                               |                                                                                                                                                                                                                                            |                              |
      |                               | Separate multiple directories with semicolons (;). You can configure up to 20 excluded directories.                                                                                                                                        | Windows: C:\\ProData         |
      +-------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------------+
      | Protected File Type           | Types of files to be protected.                                                                                                                                                                                                            | Select all                   |
      |                               |                                                                                                                                                                                                                                            |                              |
      |                               | More than 70 file formats can be protected, including databases, containers, code, certificate keys, and backups.                                                                                                                          |                              |
      |                               |                                                                                                                                                                                                                                            |                              |
      |                               | This parameter is mandatory for Linux servers only.                                                                                                                                                                                        |                              |
      +-------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------------+

#. Confirm the policy information and click **OK**.

Deleting a Policy
-----------------

#. Log in to the management console and go to the HSS page.
#. In the navigation pane, choose **Prevention** > **Ransomware Prevention**. Click the **Policies** tab.
#. Click **Delete** in the **Operation** column of the target policy.

   .. note::

      After a policy is deleted, the associated servers are no longer protected. Before deleting a policy, you are advised to bind its associated servers to other policies.

#. Confirm the policy information and click **OK**.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

:original_name: hss_01_0147.html

.. _hss_01_0147:

Viewing and Processing Baseline Check Results
=============================================

This topic provides suggestions on how to fix baseline configuration risks on the server.

Constraints
-----------

Only enterprise edition, premium edition, web tamper protection edition, and container edition are supported.

Viewing Baseline Check Overview Information
-------------------------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane on the left, choose **Prediction** > **Baseline Checks**.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.

#. Click different tabs on the displayed page to check detected unsafe configurations. :ref:`Figure 1 <hss_01_0147__table415319491112>` lists the corresponding parameters.

   To view the check results of servers under different manual baseline check policies, you can switch between baseline check policies.


   .. figure:: /_static/images/en-us_image_0000002087083905.png
      :alt: **Figure 1** Baseline check overview

      **Figure 1** Baseline check overview

   .. _hss_01_0147__table415319491112:

   .. table:: **Table 1** Baseline check overview

      +------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                          | Description                                                                                                                                                                |
      +====================================+============================================================================================================================================================================+
      | Baseline check policy              | Available baseline check policies that have been added. You can select, create, edit, and delete these policies.                                                           |
      +------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Scanned servers                    | Total number of detected servers.                                                                                                                                          |
      +------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Security baselines                 | Number of baselines executed during the server detection.                                                                                                                  |
      +------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Baseline check items               | Total number of checked server configuration items.                                                                                                                        |
      +------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Safe settings rate                 | Percentage of configuration items that passed the baseline check to the total number of check items. Failed items are displayed by risk level.                             |
      +------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Top 5 servers with unsafe settings | Statistics on servers with server configuration risks.                                                                                                                     |
      |                                    |                                                                                                                                                                            |
      |                                    | The top 5 servers with the highest risks are preferentially sorted. If no high-risk settings exist, the servers are sorted into medium-risk and low-risk ones in sequence. |
      +------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Servers with weak passwords        | Total number of detected servers, as well as the numbers of servers with weak passwords, those without weak passwords, and those with weak password detection disabled.    |
      +------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Top 5 servers with weak passwords  | Statistics on the top 5 servers with most weak password risks.                                                                                                             |
      +------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Unsafe configuration               | Alarms generated for servers with configuration risks and the risk statistics.                                                                                             |
      +------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Password complexity policies       | Statistics on servers with passwords that do not meet the complexity requirements in the baseline.                                                                         |
      +------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Common weak passwords              | Statistics on servers with weak passwords and accounts.                                                                                                                    |
      +------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Viewing and Processing Configuration Check Results
--------------------------------------------------

#. Click the **Unsafe Configurations** tab to view the risk items. For more information, see :ref:`Table 2 <hss_01_0147__table134691656201019>`.

   .. _hss_01_0147__table134691656201019:

   .. table:: **Table 2** Parameter description

      +-----------------------------------+-----------------------------------------------------------------------+
      | Parameter                         | Description                                                           |
      +===================================+=======================================================================+
      | Risk Level                        | Level of a detection result.                                          |
      |                                   |                                                                       |
      |                                   | -  High                                                               |
      |                                   | -  Low                                                                |
      |                                   | -  Medium                                                             |
      |                                   | -  Secure                                                             |
      +-----------------------------------+-----------------------------------------------------------------------+
      | Baseline Name                     | Name of the baseline that is checked.                                 |
      +-----------------------------------+-----------------------------------------------------------------------+
      | Type                              | Policy type of the baseline that has been checked.                    |
      |                                   |                                                                       |
      |                                   | -  Cloud security practices                                           |
      |                                   | -  DJCP MLPS                                                          |
      +-----------------------------------+-----------------------------------------------------------------------+
      | Check Item                        | Total number of configuration items that are checked.                 |
      +-----------------------------------+-----------------------------------------------------------------------+
      | Risky Item                        | Total number of the risky configurations.                             |
      +-----------------------------------+-----------------------------------------------------------------------+
      | Affected Servers                  | Total number of servers affected by the detected risks in a baseline. |
      +-----------------------------------+-----------------------------------------------------------------------+
      | Last Scanned                      | Time when the last detection was performed.                           |
      +-----------------------------------+-----------------------------------------------------------------------+
      | Description                       | Description of a baseline.                                            |
      +-----------------------------------+-----------------------------------------------------------------------+

#. Click the target baseline name in the list to view the baseline description, affected servers, and details about all check items.


   .. figure:: /_static/images/en-us_image_0000002071720922.png
      :alt: **Figure 2** Viewing baseline check details

      **Figure 2** Viewing baseline check details

#. Handle risk items.

   -  **Ignoring risks**

      Click **Ignore** in the **Operation** column of the target check item to ignore a check item. Select multiple check items and click **Ignore** to ignore them in batches.


      .. figure:: /_static/images/en-us_image_0000002071721090.png
         :alt: **Figure 3** Ignoring risks

         **Figure 3** Ignoring risks

   -  **Fixing risks**

      a. Click **View Details** in the **Operation** column of the target risk item to view the check item details.

      b. View the content in the **Audit Description**, **Suggestion**, and **Affected Servers**. Rectify the unsafe configurations.

         .. note::

            -  You are advised to fix the settings with high severity immediately and fix those with medium or low severity.

      c. After the repair is complete, click **Verify** on the **Affected Servers** tab page to verify the result.

         If a failed check item has been fixed, you can update its status through verification.

         .. note::

            -  Currently, baseline checks are not supported for Windows OSs.
            -  The agent status of the target server must be online.
            -  Only one risk item can be verified at a time. Other risk items can be verified only after the risk items are verified.
            -  Baseline checks are supported for the following Linux OSs: Apache 2, Docker, MongoDB, Redis, MySQL 5, Nginx, Tomcat, SSH, vsftp, CentOS 6, CentOS 7, CentOS 8, EulerOS, Debian 9, Debian 10, Debian 11, Red Hat 6, Red Hat 7, Red Hat 8, Ubuntu 12, Ubuntu 14, Ubuntu 16, Ubuntu 18.

      d. Click **Verify**.

      e. Return to the check item list page and view the status of the risk item.

         The status changes to **Verifying**. The system starts automatic verification. After the verification is complete, check the status. If a check item failed to be fixed, click **View Cause** to view the cause. Then, fix it again.

Viewing and Processing the Password Complexity Policy Detection Result
----------------------------------------------------------------------

#. Click the **Password Complexity Policy Detection** tab to view the risk statistical items and handling suggestions. For more information, see :ref:`Table 3 <hss_01_0147__table14462543144512>`.

   .. _hss_01_0147__table14462543144512:

   .. table:: **Table 3** Parameter description

      +-----------------------------------+------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                          |
      +===================================+======================================================================================================+
      | Server Name                       | Name and IP address of the detected server.                                                          |
      +-----------------------------------+------------------------------------------------------------------------------------------------------+
      | Password Length                   | Whether the password length policy of the target server meets the requirements.                      |
      |                                   |                                                                                                      |
      |                                   | -  Passed                                                                                            |
      |                                   | -  Failed                                                                                            |
      +-----------------------------------+------------------------------------------------------------------------------------------------------+
      | Uppercase Letters                 | Whether the uppercase letter policy used for passwords on the target server meets the requirements.  |
      |                                   |                                                                                                      |
      |                                   | -  Passed                                                                                            |
      |                                   | -  Failed                                                                                            |
      +-----------------------------------+------------------------------------------------------------------------------------------------------+
      | Lowercase Letters                 | Whether the lowercase letter policy used for passwords on the target server meets the requirements.  |
      |                                   |                                                                                                      |
      |                                   | -  Passed                                                                                            |
      |                                   | -  Failed                                                                                            |
      +-----------------------------------+------------------------------------------------------------------------------------------------------+
      | Digits                            | Whether the numeric policy used for passwords on the target server meets the requirements.           |
      |                                   |                                                                                                      |
      |                                   | -  Passed                                                                                            |
      |                                   | -  Failed                                                                                            |
      +-----------------------------------+------------------------------------------------------------------------------------------------------+
      | Special Characters                | Whether the special character policy used for passwords on the target server meets the requirements. |
      |                                   |                                                                                                      |
      |                                   | -  Passed                                                                                            |
      |                                   | -  Failed                                                                                            |
      +-----------------------------------+------------------------------------------------------------------------------------------------------+
      | Suggestion                        | Suggestion for the password complexity policy of the target server.                                  |
      +-----------------------------------+------------------------------------------------------------------------------------------------------+

#. Modify the password complexity policy on the server as recommended.

#. After modifying the password complexity policy, perform a manual check in the upper part of the **Baseline Checks** page to verify the result.

   If you do not perform a manual verification, HSS will automatically check the settings at 00:00:00 the next day.

Viewing and Processing Common Weak Password Detection Results
-------------------------------------------------------------

#. Click the Common Weak Password Detection tab to view the statistics of risky weak password accounts on the server. For more information, see :ref:`Viewing common weak password detection <hss_01_0147__table34521611135818>`.

   .. _hss_01_0147__table34521611135818:

   .. table:: **Table 4** Parameter description

      +-----------------------+----------------------------------------------------------------------+
      | Parameter             | Description                                                          |
      +=======================+======================================================================+
      | Server Name           | Name and IP address of the scanned server.                           |
      +-----------------------+----------------------------------------------------------------------+
      | Account Name          | Accounts with weak passwords that are detected on the target server. |
      +-----------------------+----------------------------------------------------------------------+
      | Account Type          | Type of an account.                                                  |
      +-----------------------+----------------------------------------------------------------------+
      | Usage Duration (Days) | Period for using a weak password.                                    |
      +-----------------------+----------------------------------------------------------------------+

#. Log in to the server and change the weak password.

   .. note::

      -  To enhance server security, you are advised to modify the accounts with weak passwords in a timely manner, such as SSH accounts.
      -  To protect internal data of your server, you are advised to modify software accounts that use weak passwords, such as MySQL accounts and FTP accounts.

      -  A password should contain more than eight characters, including uppercase letters, lowercase letters, digits, and special characters.

#. After the weak password is changed, perform a manual check in the upper part of the **Baseline Checks** page to verify the result.

   If you do not perform a manual verification, HSS will automatically check the settings at 00:00:00 the next day.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

:original_name: hss_01_0044.html

.. _hss_01_0044:

Configuring Policies
====================

After HSS is enabled, you can configure HSS policies based on your service requirements.

Constraints
-----------

-  The enterprise, premium, WTP, or container edition is enabled.
-  For the default policy groups, you are advised to retain their default configurations.
-  Modifications on a policy take effect only in the group it belongs to.

Accessing the Policies Page
---------------------------

#. Log in to the management console.
#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

3. In the navigation tree on the left, choose **Security Operation** > **Policies**. On the displayed page, :ref:`Policy group parameters <hss_01_0044__hss_01_0368_hss_01_0045_t801bc5e996a743dd8e2bfeb480ff1ca8>` describes the fields.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.

   .. _hss_01_0044__hss_01_0368_hss_01_0045_t801bc5e996a743dd8e2bfeb480ff1ca8:

   .. table:: **Table 1** Policy group parameters

      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                                        |
      +===================================+====================================================================================================================================================================================+
      | Policy Group                      | Name of a policy group The preset policy group names are as follows:                                                                                                               |
      |                                   |                                                                                                                                                                                    |
      |                                   | -  **tenant_linux_container_default_policy_group**: preset Linux policy of the container edition. You can copy this policy group and create a new one based on it.                 |
      |                                   | -  **tenant_linux_enterprise_default_policy_group** is the default Linux policy of the enterprise edition. This policy group can only be viewed, and cannot be copied or deleted.  |
      |                                   | -  **tenant_windows_enterprise_default_policy_group**: preset Windows policy of the enterprise edition. This policy group can only be viewed, and cannot be copied or deleted.     |
      |                                   | -  **tenant_linux_premium_default_policy_group**: preset Linux policy of the premium edition. You can create a policy group by copying this default group and modify the copy.     |
      |                                   | -  **tenant_windows_premium_default_policy_group**: preset Windows policy of the premium edition. You can create a policy group by copying this default group and modify the copy. |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | ID                                | Unique ID of a policy group                                                                                                                                                        |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Description                       | Description of a policy group                                                                                                                                                      |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Supported Version                 | HSS edition supported by a policy group.                                                                                                                                           |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Associated Servers                | To view details about the servers associated with a policy group, click the number in the **Servers** column of the group.                                                         |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

4. Click the name of the policy group to access the policy detail list.

   .. note::

      You can click **Enable** or **Disable** in the **Operation** column of a policy. After a policy is disabled, the detection of the policy is not performed.

5. You can modify the policy by clicking its name.

.. _hss_01_0044__section1219861342:

Asset Discovery
---------------

#. Click **Asset Discovery**.

#. On the displayed page, modify the settings as required. For more information, see :ref:`Table 2 <hss_01_0044__table5229440549>`.


   .. figure:: /_static/images/en-us_image_0000001670439437.png
      :alt: **Figure 1** Modifying the asset discovery policy

      **Figure 1** Modifying the asset discovery policy

   .. _hss_01_0044__table5229440549:

   .. table:: **Table 2** Parameter description

      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                      |
      +===================================+==================================================================================================================================+
      | Software Scanned                  | -  Software name. A name can contain a maximum of 5,000 characters without any space. Use commas (,) to separate software names. |
      |                                   | -  If this parameter is not specified, information about all installed software will be retrieved as its value.                  |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------+
      | Software Search Path              | Path for software search. This parameter is not required for Windows servers.                                                    |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------+
      | Scanned Web Directories           | Specifies a web directory to be scanned.                                                                                         |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------+
      | Scanned Web Directory Depth       | Specifies the level depth for web directory scanning.                                                                            |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------+

#. Confirm the information and click **OK**.

.. _hss_01_0044__section2225201363514:

Weak Password Scan
------------------

Weak passwords are not attributed to a certain type of vulnerabilities, but they bring no less security risks than any type of vulnerabilities. Data and programs will become insecure if their passwords are cracked.

HSS proactively detects the accounts using weak passwords and generates alarms for the accounts. You can also add a password that may have been leaked to the weak password list to prevent server accounts from using the password.

#. Click **Weak Password Detection**.

#. In the **Policy Settings** area, modify the settings as required. For more information, see :ref:`Table 3 <hss_01_0044__table68786563367>`.


   .. figure:: /_static/images/en-us_image_0000001670239397.png
      :alt: **Figure 2** Modifying the weak password detection policy

      **Figure 2** Modifying the weak password detection policy

   .. _hss_01_0044__table68786563367:

   .. table:: **Table 3** Parameter description

      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                         |
      +===================================+=====================================================================================================================================+
      | Scan Time                         | Time point when detections are performed. It can be accurate to the minute.                                                         |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------+
      | Random Deviation Time (s)         | Random deviation time of the weak password based on **Scan Time**. The value range is 0 to 7200s.                                   |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------+
      | Scan Days                         | Days in a week when weak passwords are scanned. You can select one or more days.                                                    |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------+
      | Detection Break Time (ms)         | Interval between the checks of two accounts. The value range is 0 to 2,000.                                                         |
      |                                   |                                                                                                                                     |
      |                                   | For example, if this parameter is set to **50**, the system checks **/bin/ls** every 50 milliseconds.                               |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------+
      | User-defined Weak Passwords       | You can add a password that may have been leaked to this weak password text box to prevent server accounts from using the password. |
      |                                   |                                                                                                                                     |
      |                                   | Enter only one weak password per line. Up to 300 weak passwords can be added.                                                       |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------+

#. Confirm the information and click **OK**.

.. _hss_01_0044__section6401323142512:

Configuration Check
-------------------

#. Click **Configuration Check**.

#. On the **Configure Check**, modify the policy.


   .. figure:: /_static/images/en-us_image_0000001621799506.png
      :alt: **Figure 3** Modifying the configuration check policy

      **Figure 3** Modifying the configuration check policy

   .. table:: **Table 4** Parameter description

      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                                         |
      +===================================+=====================================================================================================================================================================================+
      | Scan Time                         | Time point when detections are performed. It can be accurate to the minute.                                                                                                         |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Random Deviation Time (Seconds)   | Random deviation time of the system detection. The value ranges from 0 to 7,200s.                                                                                                   |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Scan Days                         | Day in a week when a detection is performed. You can select any days from Monday to Sunday.                                                                                         |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | System Default Baseline Library   | The detection baseline has been configured in the system. You only need to select the baseline you want to scan. All parameters are in their default values and cannot be modified. |
      |                                   |                                                                                                                                                                                     |
      |                                   | The parameters are as follows:                                                                                                                                                      |
      |                                   |                                                                                                                                                                                     |
      |                                   | -  **Scan**: You can select this check box to execute the corresponding baseline policy. By default, this check box is not selected.                                                |
      |                                   | -  **Baseline Name**                                                                                                                                                                |
      |                                   | -  **Type**                                                                                                                                                                         |
      |                                   | -  **Baseline Library Hash**                                                                                                                                                        |
      |                                   | -  **Keyword**                                                                                                                                                                      |
      |                                   | -  **OS Type**                                                                                                                                                                      |
      |                                   | -  **OS Name**: name of the OS to be checked. This parameter is left empty by default.                                                                                              |
      |                                   | -  **Allowed Executable Item ID**: executable items allowed during baseline detection. This parameter is left empty by default.                                                     |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Select the baseline to be detected or customize a baseline.

#. Confirm the information and click **OK**.

.. _hss_01_0044__section1575063012457:

Web Shell Detection
-------------------

If **User-defined Scan Paths** is not specified, the website paths in your assets are scanned by default. If **User-defined Scan Paths** is specified, only the specified paths are scanned.

#. Click **Web Shell Detection**.

#. On the **Web Shell Detection** page, modify the settings as required. For more information, see :ref:`Table 5 <hss_01_0044__table98811231420>`.


   .. figure:: /_static/images/en-us_image_0000001670319513.png
      :alt: **Figure 4** Modifying the web shell detection policy

      **Figure 4** Modifying the web shell detection policy

   .. _hss_01_0044__table98811231420:

   .. table:: **Table 5** Parameter description

      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                       |
      +===================================+===================================================================================================================+
      | Scan Time                         | Time point when detections are performed. It can be accurate to the minute.                                       |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------+
      | Random Deviation Time (Seconds)   | Random deviation time. The value ranges from 0 to 7,200s.                                                         |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------+
      | Scan Days                         | Days in a week when web shells are scanned. You can select one or more days.                                      |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------+
      | User-defined Scan Paths           | Web paths to be scanned. A file path must:                                                                        |
      |                                   |                                                                                                                   |
      |                                   | -  Start with a slash (/) and end with no slashes (/).                                                            |
      |                                   | -  Occupy a separate line and cannot contain spaces.                                                              |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------+
      | Monitored Files Types             | Extensions of files to be checked. Valid values include **jsp**, **jspx**, **jspf**, **php**, **php5**, **php4**. |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------+

#. Confirm the information and click **OK**.

.. _hss_01_0044__section189931229171012:

File Protection
---------------

#. Click **File Protection**.

#. On the **File Protection** page, modify the policy. For more information, see :ref:`Table 6 <hss_01_0044__table9079559112933>`.


   .. figure:: /_static/images/en-us_image_0000001621479770.png
      :alt: **Figure 5** Modifying the file protection policy

      **Figure 5** Modifying the file protection policy

   .. _hss_01_0044__table9079559112933:

   .. table:: **Table 6** Parameter description

      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                                                              |
      +===================================+==========================================================================================================================================================================================================+
      | File Privilege Escalation         | -  Detects privilege escalation.                                                                                                                                                                         |
      |                                   |                                                                                                                                                                                                          |
      |                                   |    -  |image2|: enabled                                                                                                                                                                                  |
      |                                   |    -  |image3|: disabled                                                                                                                                                                                 |
      |                                   |                                                                                                                                                                                                          |
      |                                   | -  **Ignored File Path**: Files to be ignored. Start the path with a slash (/) and do not end it with a slash (/). Each path occupies a line. No spaces are allowed between path names.                  |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | File Integrity                    | -  Detects the integrity of key files.                                                                                                                                                                   |
      |                                   |                                                                                                                                                                                                          |
      |                                   |    -  |image4|: enabled                                                                                                                                                                                  |
      |                                   |    -  |image5|: disabled                                                                                                                                                                                 |
      |                                   |                                                                                                                                                                                                          |
      |                                   | -  **File Paths**: Configure the file paths.                                                                                                                                                             |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Important File Directory Change   | -  Detects the directory change of key files.                                                                                                                                                            |
      |                                   |                                                                                                                                                                                                          |
      |                                   |    -  |image6|: enabled                                                                                                                                                                                  |
      |                                   |    -  |image7|: disabled                                                                                                                                                                                 |
      |                                   |                                                                                                                                                                                                          |
      |                                   | -  **Enable Audit**: enables the audit detection function. If the function is enabled and inotify usage exceeds the limit, some file directory changes cannot be detected.                               |
      |                                   |                                                                                                                                                                                                          |
      |                                   |    -  |image8|: enabled                                                                                                                                                                                  |
      |                                   |    -  |image9|: disabled                                                                                                                                                                                 |
      |                                   |                                                                                                                                                                                                          |
      |                                   | -  **Session IP Whitelist**: If the file process belongs to the sessions of the listed IP addresses, no audit applies.                                                                                   |
      |                                   | -  **Unmonitored File Types**: File types that do not need to be monitored.                                                                                                                              |
      |                                   | -  **Unmonitored File Paths**: File paths that do not need to be monitored.                                                                                                                              |
      |                                   | -  **Monitoring Login Keys**: enables the function of monitoring login keys.                                                                                                                             |
      |                                   |                                                                                                                                                                                                          |
      |                                   |    -  |image10|: enabled                                                                                                                                                                                 |
      |                                   |    -  |image11|: disabled                                                                                                                                                                                |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Directory Monitoring Mode         | -  Directory monitoring mode.                                                                                                                                                                            |
      |                                   | -  **File or Directory Path**: Some file or directory monitoring paths are preset in the system. You can modify the file change type to be detected and add the file or directory paths to be monitored. |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Confirm the information and click **OK**.

Login Security Check
--------------------

#. Click **Login Security Check**.

#. In the displayed **Login Security Check** page, modify the policy content. describes the parameters.


   .. figure:: /_static/images/en-us_image_0000001670559393.png
      :alt: **Figure 6** Modifying the security check policy

      **Figure 6** Modifying the security check policy

   .. table:: **Table 7** Parameter description

      +--------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                                                    | Description                                                                                                                                                                                                                                                                              |
      +==============================================================+==========================================================================================================================================================================================================================================================================================+
      | Block Attacking IP Address                                   | After the function of blocking attacking IP addresses is enabled, HSS blocks the brute-force IP address logins.                                                                                                                                                                          |
      |                                                              |                                                                                                                                                                                                                                                                                          |
      |                                                              | The agent modifies system configurations to block the source IP addresses of account cracking attacks.                                                                                                                                                                                   |
      |                                                              |                                                                                                                                                                                                                                                                                          |
      |                                                              | -  |image12|: enabled                                                                                                                                                                                                                                                                    |
      |                                                              | -  |image13|: disabled                                                                                                                                                                                                                                                                   |
      +--------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Lock Time (Min.)                                             | This parameter is used to determine how many minutes the brute-force attacks are locked. The value range is 1 to 43,200 min. (Login is not allowed in the lockout duration.)                                                                                                             |
      +--------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Cracking Behavior Determination Threshold (s)                | This parameter is used together with **Cracking Behavior Determination Threshold (Login Attempts)**. The value range is 5 to 3,600.                                                                                                                                                      |
      |                                                              |                                                                                                                                                                                                                                                                                          |
      |                                                              | For example, if this parameter is set to **30** and **Cracking Behavior Determination Threshold (Login Attempts)** is set to **5**, the system determines that an account is cracked when the same IP address fails to log in to the system for five times within 30 seconds.            |
      +--------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Cracking Behavior Determination Threshold (Login Attempts)   | This parameter is used together with **Cracking Behavior Determination Threshold**. The value range is 1 to 36,000.                                                                                                                                                                      |
      +--------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Threshold for slow brute force attack (second)               | This parameter is used together with **Threshold for slow brute force attack (failed login attempt)**. The value range is 600 to 86,400s.                                                                                                                                                |
      |                                                              |                                                                                                                                                                                                                                                                                          |
      |                                                              | For example, if this parameter is set to **3600** and **Threshold for slow brute force attack (failed login attempt)** is set to **15**, the system determines that an account is cracked when the same IP address fails to log in to the system for fifteen times within 3,600 seconds. |
      +--------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Threshold for slow brute-force attack (failed login attempt) | This parameter is used together with **Threshold for slow brute force attack (second)**. The value range is 6 to 100.                                                                                                                                                                    |
      +--------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Cracking Behavior Determination Release Time (s)             | Interval for clearing login failure records generated due to cracking. The value range is 60 to 86,400s.                                                                                                                                                                                 |
      |                                                              |                                                                                                                                                                                                                                                                                          |
      |                                                              | The unblocked IP addresses are those that triggered brute-force alarms.                                                                                                                                                                                                                  |
      +--------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Check Whether the Audit Login Is Successful                  | -  After this function is enabled, HSS reports login success logs.                                                                                                                                                                                                                       |
      |                                                              |                                                                                                                                                                                                                                                                                          |
      |                                                              |    -  |image14|: enabled                                                                                                                                                                                                                                                                 |
      |                                                              |    -  |image15|: disabled                                                                                                                                                                                                                                                                |
      +--------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Confirm the information and click **OK**.

Malicious File Detection
------------------------

#. Click **Malicious File Detection**.

#. On the displayed page, modify the policy. For more information, see :ref:`Table 8 <hss_01_0044__table180693445019>`.


   .. figure:: /_static/images/en-us_image_0000001621479778.png
      :alt: **Figure 7** Modifying the malicious file detection policy

      **Figure 7** Modifying the malicious file detection policy

   .. _hss_01_0044__table180693445019:

   .. table:: **Table 8** Parameter description

      +----------------------------------------+------------------------------------------------------------------------------------------------------------+
      | Parameter                              | Description                                                                                                |
      +========================================+============================================================================================================+
      | Whitelist Paths in Reverse Shell Check | Process file path to be ignored in reverse shell detection                                                 |
      |                                        |                                                                                                            |
      |                                        | Start with a slash (/) and end with no slashes (/). Occupy a separate line and cannot contain spaces.      |
      +----------------------------------------+------------------------------------------------------------------------------------------------------------+
      | Reverse Shell Scanning Interval (s):   | Reverse shell scanning period. The value range is 30 to 86,400.                                            |
      +----------------------------------------+------------------------------------------------------------------------------------------------------------+
      | Audit detection enhancement            | -  Whether to enhance audit detection. You are advised to enable this function.                            |
      |                                        |                                                                                                            |
      |                                        |    -  |image16|: enabled                                                                                   |
      |                                        |    -  |image17|: disabled                                                                                  |
      +----------------------------------------+------------------------------------------------------------------------------------------------------------+
      | Max. open files per process            | Maximum number of files that can be opened by a process. The value range is 10 to 300,000.                 |
      +----------------------------------------+------------------------------------------------------------------------------------------------------------+
      | Detect Reverse Shells                  | -  Detects reverse shells. You are advised to enable it.                                                   |
      |                                        |                                                                                                            |
      |                                        |    -  |image18|: enabled                                                                                   |
      |                                        |    -  |image19|: disabled                                                                                  |
      +----------------------------------------+------------------------------------------------------------------------------------------------------------+
      | Auto-block Reverse Shells              | Specifies whether to enable automatic blocking of reverse shells. You are advised to enable this function. |
      +----------------------------------------+------------------------------------------------------------------------------------------------------------+
      | Abnormal Shell Detection               | -  Detects abnormal shells. You are advised to enable it.                                                  |
      |                                        |                                                                                                            |
      |                                        |    -  |image20|: enabled                                                                                   |
      |                                        |    -  |image21|: disabled                                                                                  |
      +----------------------------------------+------------------------------------------------------------------------------------------------------------+

#. Confirm the information and click **OK**.

Abnormal Process Behavior
-------------------------

#. Click **Abnormal process behaviors**.

#. In the displayed area, modify the settings as required. For more information, see :ref:`Table 9 <hss_01_0044__table1583614466312>`.


   .. figure:: /_static/images/en-us_image_0000001670319525.png
      :alt: **Figure 8** Modifying the abnormal process behavior policy

      **Figure 8** Modifying the abnormal process behavior policy

   .. _hss_01_0044__table1583614466312:

   .. table:: **Table 9** Parameter description

      +----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
      | Parameter                              | Description                                                                                                                                                                                            | Example Value         |
      +========================================+========================================================================================================================================================================================================+=======================+
      | Detection and Scanning Cycle (Seconds) | Interval for checking the running programs on the host. The value range is 30 to 1,800.                                                                                                                | 1800                  |
      +----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
      | Detection Mode                         | Select the method for abnormal process behavior detection.                                                                                                                                             | Balanced              |
      |                                        |                                                                                                                                                                                                        |                       |
      |                                        | -  **Sensitive**: In-depth and full detection and scanning are performed on all processes, which may cause false positives. Suitable for cyber protection drills and key event assurance drills.       |                       |
      |                                        | -  **Balanced**: All processes are detected and scanned. The detection result accuracy and the abnormal process detection rate are balanced. Suitable for routine protection.                          |                       |
      |                                        | -  **Conservative**: All processes are detected and scanned. This mode provides high detection result accuracy and low false positives. Suitable for scenarios with a large number of false positives. |                       |
      +----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
      | Threshold for Score Reporting          | Score reporting threshold. The value range is 1 to 100.                                                                                                                                                | 3                     |
      +----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+

#. Confirm the information and click **OK**.

Root Privilege Escalation Detection
-----------------------------------

#. Click **Root privilege escalation**.

#. In the displayed area, modify the settings as required. For more information, see :ref:`Table 10 <hss_01_0044__table168831222885>`.


   .. figure:: /_static/images/en-us_image_0000001621479782.png
      :alt: **Figure 9** Modifying the root privilege escalation policy

      **Figure 9** Modifying the root privilege escalation policy

   .. _hss_01_0044__table168831222885:

   .. table:: **Table 10** Parameter description

      +-----------------------------------+-------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                           |
      +===================================+=======================================================================================================+
      | Ignored Process File Path         | Ignored process file path                                                                             |
      |                                   |                                                                                                       |
      |                                   | Start with a slash (/) and end with no slashes (/). Occupy a separate line and cannot contain spaces. |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------+
      | Scanning Interval (s)             | Interval for checking process files. The value range is 5 to 3,600.                                   |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------+

#. Confirm the information and click **OK**.

Real-time Process
-----------------

#. Click **Real-time Process**.

#. On the displayed page, modify the settings as required. For more information, see :ref:`Table 11 <hss_01_0044__table11629197163518>`.


   .. figure:: /_static/images/en-us_image_0000001676837385.png
      :alt: **Figure 10** Modifying the real-time process policy

      **Figure 10** Modifying the real-time process policy

   .. _hss_01_0044__table11629197163518:

   .. table:: **Table 11** Parameters for real-time process policy settings

      +----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                        | Description                                                                                                                                                                                   |
      +==================================+===============================================================================================================================================================================================+
      | Full Process Report Interval (s) | Interval for reporting the full process. The value range is 3,600 to 86,400.                                                                                                                  |
      +----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | High-Risk Commands               | High-risk commands that contain keywords during detection.                                                                                                                                    |
      +----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Whitelist (Do Not Record Logs)   | Paths or programs that are allowed or ignored during detection. You can enter the regular expression of the command to be added to the whitelist. The command regular expression is optional. |
      +----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Confirm the information and click **OK**.

Rootkit Detection
-----------------

#. Click **Rootkit Detection**.

#. On the rootkit detection page, modify the policy content.


   .. figure:: /_static/images/en-us_image_0000001621959490.png
      :alt: **Figure 11** Modifying the rootkit detection policy

      **Figure 11** Modifying the rootkit detection policy

   .. table:: **Table 12** Parameter description

      +-------------------------+-------------------------------------------------------------------------------------------------------------------+-----------------------+
      | Parameter               | Description                                                                                                       | Example Value         |
      +=========================+===================================================================================================================+=======================+
      | Scanning Interval (s)   | Interval for executing the check policy. The value ranges from 60 to 86,400.                                      | 86400                 |
      +-------------------------+-------------------------------------------------------------------------------------------------------------------+-----------------------+
      | Check Library           | Check files and folders in the existing libraries. You are advised to enable this function.                       | |image24|: enabled    |
      |                         |                                                                                                                   |                       |
      |                         | -  |image22|: enabled                                                                                             |                       |
      |                         | -  |image23|: disabled                                                                                            |                       |
      +-------------------------+-------------------------------------------------------------------------------------------------------------------+-----------------------+
      | Check Kernel Space      | Perform the check by kernel modules. All kernel modules will be checked. You are advised to enable this function. | |image27|: enabled    |
      |                         |                                                                                                                   |                       |
      |                         | -  |image25|: enabled                                                                                             |                       |
      |                         | -  |image26|: disabled                                                                                            |                       |
      +-------------------------+-------------------------------------------------------------------------------------------------------------------+-----------------------+
      | Kernel Module Whitelist | Add the kernel modules that can be ignored during the detection.                                                  | xt_conntrack          |
      |                         |                                                                                                                   |                       |
      |                         | Up to 10 kernel modules can be added. Each module occupies a line.                                                | virtio_scsi           |
      |                         |                                                                                                                   |                       |
      |                         |                                                                                                                   | tun                   |
      +-------------------------+-------------------------------------------------------------------------------------------------------------------+-----------------------+

#. Confirm the information and click **OK**.

AV Detection
------------

#. Click **AV Detection**.

#. On the **AV Detection** slide pane that is displayed, modify the settings as required. For details, see :ref:`Table 13 <hss_01_0044__table394917175383>`.


   .. figure:: /_static/images/en-us_image_0000001670559401.png
      :alt: **Figure 12** Modifying an AV detection policy

      **Figure 12** Modifying an AV detection policy

   .. _hss_01_0044__table394917175383:

   .. table:: **Table 13** AV detection policy parameters

      +-----------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
      | Parameter             | Description                                                                                                                                          | Example Value         |
      +=======================+======================================================================================================================================================+=======================+
      | Real-Time Protection  | After this function is enabled, AV detection is performed in real time when the current policy is executed. You are advised to enable this function. | |image30|: enabled    |
      |                       |                                                                                                                                                      |                       |
      |                       | -  |image28|: enabled                                                                                                                                |                       |
      |                       | -  |image29|: disabled                                                                                                                               |                       |
      +-----------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
      | Protected File Type   | Type of the files to be checked in real time.                                                                                                        | All                   |
      |                       |                                                                                                                                                      |                       |
      |                       | -  **All**: Select all file types.                                                                                                                   |                       |
      |                       | -  **Executable**: Executable file types such as EXE, DLL, and SYS.                                                                                  |                       |
      |                       | -  **Compressed**: Compressed file types such as ZIP, RAR, and JAR.                                                                                  |                       |
      |                       | -  **Text**: Text file types such as PHP, JSP, HTML, and Bash.                                                                                       |                       |
      |                       | -  **OLE**: Composite file types such as Microsoft Office files (PPT and DOC) and saved email files (MSG).                                           |                       |
      |                       | -  **Other**: File types except the preceding types.                                                                                                 |                       |
      +-----------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
      | Action                | Handling method for the object detection alarms.                                                                                                     | Automatic handling    |
      |                       |                                                                                                                                                      |                       |
      |                       | -  **Automated handling**:Isolate high-risk virus files bu default. Report other virus files but do not isolate them.                                |                       |
      |                       | -  **Manual handling**: Report all the detected virus files but do not isolate them. You need to handle them manually.                               |                       |
      +-----------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+

#. Confirm the information and click **OK**.

Container Information Collection
--------------------------------

#. Click **Container Information Collection**.

#. On the **Container Information Collection** slide pane that is displayed, modify the **Policy Settings**. For details about the parameters, see :ref:`Table 14 <hss_01_0044__table199907487168>`.


   .. figure:: /_static/images/en-us_image_0000001621960166.png
      :alt: **Figure 13** Modifying the container information collection policy

      **Figure 13** Modifying the container information collection policy

   .. note::

      The whitelist has a higher priority than blacklist. If a directory is specified in both the whitelist and blacklist, it is regarded as a whitelisted item.

   .. _hss_01_0044__table199907487168:

   .. table:: **Table 14** Container information collection policy parameters

      +-----------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter             | Description                                                                                                                                                                                                     | Example Value                                                                                                                                            |
      +=======================+=================================================================================================================================================================================================================+==========================================================================================================================================================+
      | Mount Path Whitelist  | Enter the directory that can be mounted.                                                                                                                                                                        | /test/docker or /root/\*                                                                                                                                 |
      |                       |                                                                                                                                                                                                                 |                                                                                                                                                          |
      |                       |                                                                                                                                                                                                                 | Note: If a directory ends with an asterisk (``*``), it indicates all the sub-directories under the directory (excluding the main directory).             |
      |                       |                                                                                                                                                                                                                 |                                                                                                                                                          |
      |                       |                                                                                                                                                                                                                 | For example, if **/var/test/\*** is specified in the whitelist, all sub-directories in **/var/test/** are whitelisted, excluding the **test** directory. |
      +-----------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Mount Path Blacklist  | Enter the directories that cannot be mounted. For example, **user** and **bin**, the directories of key host information files, are not advised being mounted. Otherwise, important information may be exposed. |                                                                                                                                                          |
      +-----------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Confirm the information and click **OK**.

Cluster Intrusion Detection
---------------------------

#. Click **Cluster Intrusion Detection**.

#. On the **Cluster Intrusion Detection** slide pane that is displayed, modify the **Policy Settings**. For details about the parameters, see :ref:`Table 15 <hss_01_0044__table1995510152385>`.


   .. figure:: /_static/images/en-us_image_0000001670320201.png
      :alt: **Figure 14** Modifying the cluster intrusion detection policy

      **Figure 14** Modifying the cluster intrusion detection policy

   .. _hss_01_0044__table1995510152385:

   .. table:: **Table 15** Cluster intrusion detection policy parameters

      +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------+----------------------------+
      | Parameter             | Description                                                                                                                               | Example Value              |
      +=======================+===========================================================================================================================================+============================+
      | Basic Detection Cases | Select basic check items as required.                                                                                                     | Select all                 |
      +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------+----------------------------+
      | Whitelist             | You can customize the types and values that need to be ignored during the detection. You can add and delete types and values as required. | Type: IP address filtering |
      |                       |                                                                                                                                           |                            |
      |                       | The following types are supported:                                                                                                        | Value: 192.168.x.x         |
      |                       |                                                                                                                                           |                            |
      |                       | -  IP address filter                                                                                                                      |                            |
      |                       | -  Pod name filter                                                                                                                        |                            |
      |                       | -  Image name filter                                                                                                                      |                            |
      |                       | -  User filter                                                                                                                            |                            |
      |                       | -  Pod tag filter                                                                                                                         |                            |
      |                       | -  Namespace filter                                                                                                                       |                            |
      |                       |                                                                                                                                           |                            |
      |                       |    .. note::                                                                                                                              |                            |
      |                       |                                                                                                                                           |                            |
      |                       |       Each type can be used only once.                                                                                                    |                            |
      +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------+----------------------------+

   .. note::

      After this policy is configured, you need to enable the log audit function and deploy the HSS agent on the management node (node where the APIServer is located) of the cluster to make the policy take effect.

#. Confirm the information and click **OK**.

Container File Monitoring
-------------------------

.. important::

   If a monitored file path is under the mount path rather than the writable layer of the container on the server, changes on the file cannot trigger container file modification alarms. To protect such files, configure a :ref:`file protection policy <hss_01_0044__section189931229171012>`.

#. Click **Container File Monitoring**.

#. On the **Container File Monitoring** slide pane that is displayed, modify the **Policy Settings**. For details about the parameters, see :ref:`Table 16 <hss_01_0044__table9683478481>`.


   .. figure:: /_static/images/en-us_image_0000001670440105.png
      :alt: **Figure 15** Modifying the container file monitoring policy

      **Figure 15** Modifying the container file monitoring policy

   .. _hss_01_0044__table9683478481:

   .. table:: **Table 16** Container file monitoring policy parameters

      +----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+----------------+
      | Parameter            | Description                                                                                                                                                    | Example Value  |
      +======================+================================================================================================================================================================+================+
      | Fuzzy match          | Indicates whether to enable fuzzy match for the target file. You are advised to select this option.                                                            | Selected       |
      +----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+----------------+
      | Block New Executable | Monitor the behavior of the adding executable files. If this option is selected, adding executable files is prohibited. You are advised to select this option. | Selected       |
      +----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+----------------+
      | Image Name           | Name of the target image to be checked                                                                                                                         | test_bj4       |
      +----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+----------------+
      | Image ID             | ID of the target image to be checked                                                                                                                           | ``-``          |
      +----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+----------------+
      | File                 | Name of the file in the target image to be checked                                                                                                             | /tmp/testw.txt |
      +----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+----------------+

#. Confirm the information and click **OK**.

Container Process Whitelist
---------------------------

#. Click **Container Process Whitelist**.

#. On the **Container Process Whitelist** slide pane that is displayed, modify the **Policy Settings**. For details about the parameters, see :ref:`Table 17 <hss_01_0044__table1325215475552>`.


   .. figure:: /_static/images/en-us_image_0000001670240065.png
      :alt: **Figure 16** Container process whitelist policy

      **Figure 16** Container process whitelist policy

   .. _hss_01_0044__table1325215475552:

   .. table:: **Table 17** Container process whitelist policy parameters

      +-------------+-----------------------------------------------------------------------------------------------------+---------------+
      | Parameter   | Description                                                                                         | Example Value |
      +=============+=====================================================================================================+===============+
      | Fuzzy Match | Indicates whether to enable fuzzy match for the target file. You are advised to select this option. | Selected      |
      +-------------+-----------------------------------------------------------------------------------------------------+---------------+
      | Image Name  | Name of the target image to be detected                                                             | test_bj4      |
      +-------------+-----------------------------------------------------------------------------------------------------+---------------+
      | Image ID    | ID of the target image to be checked                                                                | ``-``         |
      +-------------+-----------------------------------------------------------------------------------------------------+---------------+
      | File        | Path of the file in the target image to be checked                                                  | /tmp/testw    |
      +-------------+-----------------------------------------------------------------------------------------------------+---------------+

#. Confirm the information and click **OK**.

.. _hss_01_0044__section1718012455468:

Suspicious Image Behaviors
--------------------------

#. Click **Suspicious Image Behaviors**.

#. On the **Suspicious Image Behaviors** slide pane that is displayed, modify the **Policy Settings**. For details about the parameters, see :ref:`Table 18 <hss_01_0044__table191314400575>`.


   .. figure:: /_static/images/en-us_image_0000001621480454.png
      :alt: **Figure 17** Modifying the suspicious image behavior policy

      **Figure 17** Modifying the suspicious image behavior policy

   .. _hss_01_0044__table191314400575:

   .. table:: **Table 18** Suspicious image behaviors policy parameters

      +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
      | Parameter             | Description                                                                                                                                                             | Example Value         |
      +=======================+=========================================================================================================================================================================+=======================+
      | Rule Name             | Name of a rule                                                                                                                                                          | ``-``                 |
      +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
      | Description           | Brief description of a rule                                                                                                                                             | ``-``                 |
      +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
      | Template              | -  Configure templates based on different rules. The supported rules are as follows:                                                                                    | ``-``                 |
      |                       |                                                                                                                                                                         |                       |
      |                       |    -  Image whitelist                                                                                                                                                   |                       |
      |                       |    -  Image blacklist                                                                                                                                                   |                       |
      |                       |    -  Image tag whitelist                                                                                                                                               |                       |
      |                       |    -  Image tag blacklist                                                                                                                                               |                       |
      |                       |    -  Create container whitelist                                                                                                                                        |                       |
      |                       |    -  Create container blacklist                                                                                                                                        |                       |
      |                       |    -  Container mount proc whitelist                                                                                                                                    |                       |
      |                       |    -  Container seccomp unconfined                                                                                                                                      |                       |
      |                       |    -  Container privilege whitelist                                                                                                                                     |                       |
      |                       |    -  Container capability whitelist                                                                                                                                    |                       |
      |                       |                                                                                                                                                                         |                       |
      |                       | -  The parameters are described as follows:                                                                                                                             |                       |
      |                       |                                                                                                                                                                         |                       |
      |                       |    -  **Exact match**: Enter the names of the images you want to check. Use semicolons (;) to separate multiple names. A maximum of 20 names can be entered.            |                       |
      |                       |    -  **RegEx match**: Use regular expressions to match images. Use semicolons (;) to separate multiple expressions. A maximum of 20 expressions can be entered.        |                       |
      |                       |    -  **Prefix match**: Enter the prefixes of the images you want to check. Multiple prefixes are separated by semicolons (;). A maximum of 20 prefixes can be entered. |                       |
      |                       |    -  **Tag Name**: Enter the tag and value of the images you want to check. A maximum of 20 tags can be added.                                                         |                       |
      |                       |    -  **Permission Type**: Specify permissions to be checked or ignored. For details about permissions, see :ref:`Table 19 <hss_01_0044__table16974181219484>`.         |                       |
      +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+

   .. _hss_01_0044__table16974181219484:

   .. table:: **Table 19** Abnormal image permissions

      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | Permissions Name   | Description                                                                                                                   |
      +====================+===============================================================================================================================+
      | AUDIT_WRITE        | Write records to kernel auditing log.                                                                                         |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | CHOWN              | Make arbitrary changes to file UIDs and GIDs.                                                                                 |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | DAC_OVERRIDE       | Bypass file read, write, and execute permission checks.                                                                       |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | FOWNER             | Bypass permission checks on operations that normally require the file system UID of the process to match the UID of the file. |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | FSETID             | Do not clear set-user-ID and set-group-ID permission bits when a file is modified.                                            |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | KILL               | Bypass permission checks for sending signals                                                                                  |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | MKNOD              | Create special files using mknod.                                                                                             |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | NET_BIND_SERVICE   | Bind a socket to internet domain privileged ports (port numbers less than 1024).                                              |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | NET_RAW            | Use RAW and PACKET sockets.                                                                                                   |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | SETFCAP            | Set file capabilities.                                                                                                        |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | SETGID             | Make arbitrary manipulations of process GIDs and supplementary GID list.                                                      |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | SETPCAP            | Modify process capabilities.                                                                                                  |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | SETUID             | Make arbitrary manipulations of process UIDs.                                                                                 |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | SYS_CHROOT         | Use chroot to change the root directory.                                                                                      |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | AUDIT_CONTROL      | Enable and disable kernel auditing; change auditing filter rules; retrieve auditing status and filtering rules.               |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | AUDIT_READ         | Allow reading audit logs via multicast netlink socket.                                                                        |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | BLOCK_SUSPEND      | Allow suspension prevention.                                                                                                  |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | BPF                | Allow creating BPF maps, loading BPF Type Format (BTF) data, retrieve JITed code of BPF programs, and more.                   |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | CHECKPOINT_RESTORE | Allow operations related to checkpoints and restoration.                                                                      |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | DAC_READ_SEARCH    | Bypass file read permission checks and directory read and execute permission checks.                                          |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | IPC_LOCK           | Lock memory (such as mlock, mlockall, mmap, and shmctl).                                                                      |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | IPC_OWNER          | Bypass permission checks for operations on System V IPC objects.                                                              |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | LEASE              | Establish leases on arbitrary files                                                                                           |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | LINUX_IMMUTABLE    | Set the FS_APPEND_FL and FS_IMMUTABLE_FL i-node flags.                                                                        |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | MAC_ADMIN          | Allow MAC configuration or state changes.                                                                                     |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | MAC_OVERRIDE       | Override Mandatory Access Control (MAC).                                                                                      |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | NET_ADMIN          | Perform various network-related operations.                                                                                   |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | NET_BROADCAST      | Make socket broadcasts, and listen to multicasts.                                                                             |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | PERFMON            | Allow privileged system performance and observability operations using perf_events, i915_perf and other kernel subsystems.    |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | SYS_ADMIN          | Perform a range of system administration operations.                                                                          |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | SYS_BOOT           | Use reboot and kexec_load. Reboot and load a new kernel for later execution.                                                  |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | SYS_MODULE         | Load and unload kernel modules.                                                                                               |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | SYS_NICE           | Raise process nice value (nice, set priority) and change the nice value for arbitrary processes.                              |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | SYS_PACCT          | Enable or disable process accounting.                                                                                         |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | SYS_PTRACE         | Trace arbitrary processes using ptrace.                                                                                       |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | SYS_RAWIO          | Perform I/O port operations (ipl and ioperm).                                                                                 |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | SYS_RESOURCE       | Override resource limits.                                                                                                     |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | SYS_TIME           | Set the system clock (settimeofday, stime, and adjtimex) and real-time (hardware) clock.                                      |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | SYS_TTY_CONFIG     | Use vhangup. Employ various privileged ioctl operations on virtual terminals.                                                 |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | SYSLOG             | Perform privileged syslog operations.                                                                                         |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+
      | WAKE_ALARM         | Trigger something that will wake up the system.                                                                               |
      +--------------------+-------------------------------------------------------------------------------------------------------------------------------+

#. Confirm the information and click **OK**.

Port Scan Detection
-------------------

#. Click **Port Scan Detection**.

#. On the **Port Scan Detection** slide pane that is displayed, modify the **Policy Settings**. For details about the parameters, see :ref:`Table 20 <hss_01_0044__table188451238181811>`.


   .. figure:: /_static/images/en-us_image_0000001621640278.png
      :alt: **Figure 18** Modifying the port scanning policy

      **Figure 18** Modifying the port scanning policy

   .. _hss_01_0044__table188451238181811:

   .. table:: **Table 20** Port scan detection policy parameters

      +----------------------------------------------+-------------------------------------------------------------------------------------+---------------+
      | Parameter                                    | Description                                                                         | Example Value |
      +==============================================+=====================================================================================+===============+
      | Process Information Collection Interval (s): | Interval for obtaining processes                                                    | Selected      |
      +----------------------------------------------+-------------------------------------------------------------------------------------+---------------+
      | Source IP Address Whitelist                  | Enter the IP address whitelist. Separate multiple IP addresses with semicolons (;). | test_bj4      |
      +----------------------------------------------+-------------------------------------------------------------------------------------+---------------+
      | Packet Quantity Threshold                    | ``-``                                                                               | ``-``         |
      +----------------------------------------------+-------------------------------------------------------------------------------------+---------------+
      | Ports to Scan                                | Details about the port number and protocol type to be detected                      | ``-``         |
      +----------------------------------------------+-------------------------------------------------------------------------------------+---------------+

#. Confirm the information and click **OK**.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png
.. |image2| image:: /_static/images/en-us_image_0000001621639582.png
.. |image3| image:: /_static/images/en-us_image_0000001621959478.png
.. |image4| image:: /_static/images/en-us_image_0000001670559389.png
.. |image5| image:: /_static/images/en-us_image_0000001670439441.png
.. |image6| image:: /_static/images/en-us_image_0000001670239401.png
.. |image7| image:: /_static/images/en-us_image_0000001621799510.png
.. |image8| image:: /_static/images/en-us_image_0000001670319517.png
.. |image9| image:: /_static/images/en-us_image_0000001621479774.png
.. |image10| image:: /_static/images/en-us_image_0000001621639586.png
.. |image11| image:: /_static/images/en-us_image_0000001621959482.png
.. |image12| image:: /_static/images/en-us_image_0000001670439445.png
.. |image13| image:: /_static/images/en-us_image_0000001670239405.png
.. |image14| image:: /_static/images/en-us_image_0000001621799514.png
.. |image15| image:: /_static/images/en-us_image_0000001670319521.png
.. |image16| image:: /_static/images/en-us_image_0000001621639590.png
.. |image17| image:: /_static/images/en-us_image_0000001621959486.png
.. |image18| image:: /_static/images/en-us_image_0000001670559397.png
.. |image19| image:: /_static/images/en-us_image_0000001670439449.png
.. |image20| image:: /_static/images/en-us_image_0000001670239409.png
.. |image21| image:: /_static/images/en-us_image_0000001621799518.png
.. |image22| image:: /_static/images/en-us_image_0000001686938880.png
.. |image23| image:: /_static/images/en-us_image_0000001734778037.png
.. |image24| image:: /_static/images/en-us_image_0000001686938876.png
.. |image25| image:: /_static/images/en-us_image_0000001734937861.png
.. |image26| image:: /_static/images/en-us_image_0000001686938868.png
.. |image27| image:: /_static/images/en-us_image_0000001734937857.png
.. |image28| image:: /_static/images/en-us_image_0000001670439453.png
.. |image29| image:: /_static/images/en-us_image_0000001670239413.png
.. |image30| image:: /_static/images/en-us_image_0000001686939532.png

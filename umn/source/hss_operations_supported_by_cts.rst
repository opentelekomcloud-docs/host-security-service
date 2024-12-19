:original_name: hss_01_0071.html

.. _hss_01_0071:

HSS Operations Supported by CTS
===============================

:ref:`Table 1 <hss_01_0071__table24308247181417>` provides more details.

.. _hss_01_0071__table24308247181417:

.. table:: **Table 1** HSS operations that can be recorded by CTS

   +-----------------------------------------------+---------------+-----------------------------+
   | Operation                                     | Resource Type | Trace Name                  |
   +===============================================+===============+=============================+
   | Unignoring a port                             | hss           | notIgnorePortStatus         |
   +-----------------------------------------------+---------------+-----------------------------+
   | Ignoring a port                               | hss           | ignorePortStatus            |
   +-----------------------------------------------+---------------+-----------------------------+
   | Unignoring configuration check items          | hss           | notIgnoreCheckRuleStat      |
   +-----------------------------------------------+---------------+-----------------------------+
   | Ignoring configuration check items            | hss           | ignoreCheckRuleStat         |
   +-----------------------------------------------+---------------+-----------------------------+
   | Retrying a baseline check                     | hss           | runBaselineDetect           |
   +-----------------------------------------------+---------------+-----------------------------+
   | Unbinding quota                               | hss           | cancelHostsQuota            |
   +-----------------------------------------------+---------------+-----------------------------+
   | Disabling container protection                | hss           | closeContainerProtectStatus |
   +-----------------------------------------------+---------------+-----------------------------+
   | Enabling container protection                 | hss           | openContainerProtectStatus  |
   +-----------------------------------------------+---------------+-----------------------------+
   | Unblocking an IP address                      | hss           | changeBlockedIp             |
   +-----------------------------------------------+---------------+-----------------------------+
   | Handling an event                             | hss           | changeEvent                 |
   +-----------------------------------------------+---------------+-----------------------------+
   | Canceling the isolation of a file             | hss           | changeIsolatedFile          |
   +-----------------------------------------------+---------------+-----------------------------+
   | Removing an alarm from whitelist              | hss           | removeAlarmWhiteList        |
   +-----------------------------------------------+---------------+-----------------------------+
   | Adding Login Whitelist                        | hss           | addLoginWhiteList           |
   +-----------------------------------------------+---------------+-----------------------------+
   | Removing Login Whitelist                      | hss           | removeLoginWhiteList        |
   +-----------------------------------------------+---------------+-----------------------------+
   | Adding a server group                         | hss           | addHostsGroup               |
   +-----------------------------------------------+---------------+-----------------------------+
   | Adding servers to a group                     | hss           | associateHostsGroup         |
   +-----------------------------------------------+---------------+-----------------------------+
   | Modifying a server group                      | hss           | changeHostsGroup            |
   +-----------------------------------------------+---------------+-----------------------------+
   | Deleting a server group                       | hss           | deleteHostsGroup            |
   +-----------------------------------------------+---------------+-----------------------------+
   | Disabling HSS                                 | hss           | closeHostsProtectStatus     |
   +-----------------------------------------------+---------------+-----------------------------+
   | Enabling HSS                                  | hss           | openHostsProtectStatus      |
   +-----------------------------------------------+---------------+-----------------------------+
   | Uninstalling an agent                         | hss           | uninstallAgents             |
   +-----------------------------------------------+---------------+-----------------------------+
   | Scanning an image                             | hss           | runImageScan                |
   +-----------------------------------------------+---------------+-----------------------------+
   | Synchronizing the image list from SWR         | hss           | runImageSynchronizeTask     |
   +-----------------------------------------------+---------------+-----------------------------+
   | Updating and scanning an SWR image            | hss           | runSwrImageScan             |
   +-----------------------------------------------+---------------+-----------------------------+
   | Performing a security check again             | hss           | resetRiskScore              |
   +-----------------------------------------------+---------------+-----------------------------+
   | Adding a policy group                         | hss           | addPolicyGroup              |
   +-----------------------------------------------+---------------+-----------------------------+
   | Removing a policy group                       | hss           | deletePolicyGroup           |
   +-----------------------------------------------+---------------+-----------------------------+
   | Applying a policy group                       | hss           | deployPolicyGroup           |
   +-----------------------------------------------+---------------+-----------------------------+
   | Modifying a policy                            | hss           | modifyPolicyDetail          |
   +-----------------------------------------------+---------------+-----------------------------+
   | Modifying a policy group                      | hss           | modifyPolicyGroup           |
   +-----------------------------------------------+---------------+-----------------------------+
   | Disabling automatic isolation and killing     | hss           | closeAutoKillVirusStatus    |
   +-----------------------------------------------+---------------+-----------------------------+
   | Enabling automatic isolation and killing      | hss           | openAutoKillVirusStatus     |
   +-----------------------------------------------+---------------+-----------------------------+
   | Configure common login IP addresses           | hss           | modifyLoginCommonIp         |
   +-----------------------------------------------+---------------+-----------------------------+
   | Configure common login locations              | hss           | modifyLoginCommonLocation   |
   +-----------------------------------------------+---------------+-----------------------------+
   | Configuring the SSH login whitelist           | hss           | modifyLoginWhiteIp          |
   +-----------------------------------------------+---------------+-----------------------------+
   | Fixing a vulnerability                        | hss           | changeVulStatus             |
   +-----------------------------------------------+---------------+-----------------------------+
   | Adding a protected directory                  | hss           | addHostProtectDirInfo       |
   +-----------------------------------------------+---------------+-----------------------------+
   | Adding a privileged process                   | hss           | addPrivilegedProcessInfo    |
   +-----------------------------------------------+---------------+-----------------------------+
   | Adding a scheduled protection setting         | hss           | addTimingOffConfigInfo      |
   +-----------------------------------------------+---------------+-----------------------------+
   | Removing a remote backup server               | hss           | deleteBackupHostInfo        |
   +-----------------------------------------------+---------------+-----------------------------+
   | Removing a protected directory                | hss           | deleteHostProtectDirInfo    |
   +-----------------------------------------------+---------------+-----------------------------+
   | Removing a privileged process                 | hss           | deletePrivilegedProcessInfo |
   +-----------------------------------------------+---------------+-----------------------------+
   | Deleting scheduled protection settings        | hss           | deleteTimingOffConfigInfo   |
   +-----------------------------------------------+---------------+-----------------------------+
   | Configuring the scheduled protection period   | hss           | setDateOffConfigInfo        |
   +-----------------------------------------------+---------------+-----------------------------+
   | Modifying the status of a protected directory | hss           | setProtectDirSwitchInfo     |
   +-----------------------------------------------+---------------+-----------------------------+
   | Enabling or disabling dynamic WTP             | hss           | setRaspSwitch               |
   +-----------------------------------------------+---------------+-----------------------------+
   | Configuring a remote backup server            | hss           | setRemoteBackupInfo         |
   +-----------------------------------------------+---------------+-----------------------------+
   | Enabling or disabling scheduled protection    | hss           | setTimingOffSwitchInfo      |
   +-----------------------------------------------+---------------+-----------------------------+
   | Disabling WTP                                 | hss           | closeWtpProtectionStatus    |
   +-----------------------------------------------+---------------+-----------------------------+
   | Enabling WTP                                  | hss           | openWtpProtectionStatus     |
   +-----------------------------------------------+---------------+-----------------------------+
   | Modifying a remote backup server              | hss           | updateBackupHostInfo        |
   +-----------------------------------------------+---------------+-----------------------------+
   | Modifying a protected directory               | hss           | updateHostProtectDirInfo    |
   +-----------------------------------------------+---------------+-----------------------------+
   | Modifying a privileged process                | hss           | updatePrivilegedProcessInfo |
   +-----------------------------------------------+---------------+-----------------------------+
   | Modifying the Tomcat bin directory            | hss           | updateRaspPathInfo          |
   +-----------------------------------------------+---------------+-----------------------------+
   | Modifying the scheduled protection period     | hss           | updateTimingOffConfigInfo   |
   +-----------------------------------------------+---------------+-----------------------------+

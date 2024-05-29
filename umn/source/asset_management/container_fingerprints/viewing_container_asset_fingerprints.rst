:original_name: hss_01_0465.html

.. _hss_01_0465:

Viewing Container Asset Fingerprints
====================================

HSS can collect container asset fingerprints, including container accounts, ports, and processes. You can centrally check container asset information and detect risky assets in a timely manner based on the container fingerprints. This section describes how to view collected container asset information.

Constraints
-----------

-  Only the HSS container edition supports the container fingerprint function.
-  Only Linux is supported.

Viewing Asset Fingerprints Data of All Containers
-------------------------------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

#. Choose **Asset Management** > **Container Fingerprints** > **Asset Fingerprints**. On the **Asset Fingerprints** page that is displayed, view the fingerprint data of all containers.

   If you find risky assets after counting, remove them in a timely manner. You are advised to handle the ports as follows:

   -  If HSS detects open high-risk ports or unused ports, check whether they are really used by your services. If they are not, disable them. For dangerous ports, you are advised to further check their program files, and delete or isolate their source files if necessary.
   -  If a detected high-risk port is actually a normal port used for services, you can ignore it. Ignored alarms will neither be recorded as unsafe items and nor trigger alarms.

   .. note::

      If your servers are managed by enterprise projects, you can select the target enterprise project to view or operate the asset and detection information.


   .. figure:: /_static/images/en-us_image_0000001853723125.png
      :alt: **Figure 1** Viewing container assets

      **Figure 1** Viewing container assets

   .. _hss_01_0465__table7132214184518:

   .. table:: **Table 1** Container asset fingerprints

      +-----------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------+
      | Item                  | Description                                                                                                                                                                                                                                                                                                         | Automatic Detection Period            |
      +=======================+=====================================================================================================================================================================================================================================================================================================================+=======================================+
      | Account Information   | Check and manage all accounts on your containers to keep them secure.                                                                                                                                                                                                                                               | Automatic check every hour            |
      |                       |                                                                                                                                                                                                                                                                                                                     |                                       |
      |                       | Real-time account information includes the account name, number of servers, server name, IP address, login permission, root permission, user group, user directory, shell started by the user, container name, container ID, and the last scan time.                                                                |                                       |
      +-----------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------+
      | Open Ports            | Check open ports on your containers, including risky and unknown ports.                                                                                                                                                                                                                                             | Automated check every 30 seconds      |
      |                       |                                                                                                                                                                                                                                                                                                                     |                                       |
      |                       | You can easily find high-risk ports on containers by checking local ports, protocol types, server names, IP addresses, statuses, PIDs, and program files.                                                                                                                                                           |                                       |
      |                       |                                                                                                                                                                                                                                                                                                                     |                                       |
      |                       | -  Manually disabling high-risk ports                                                                                                                                                                                                                                                                               |                                       |
      |                       |                                                                                                                                                                                                                                                                                                                     |                                       |
      |                       |    If dangerous or unnecessary ports are found enabled, check whether they are mandatory for services, and disable them if they are not. For dangerous ports, you are advised to further check their program files, and delete or isolate their source files if necessary.                                          |                                       |
      |                       |                                                                                                                                                                                                                                                                                                                     |                                       |
      |                       |    It is recommended that you handle the ports with the **Dangerous** risk level promptly and handle the ports with the **Unknown** risk level based on the actual service conditions.                                                                                                                              |                                       |
      |                       |                                                                                                                                                                                                                                                                                                                     |                                       |
      |                       | -  Ignore risks: If a detected high-risk port is actually a normal port used for services, you can ignore it. The port will no longer be regarded risky or generate alarms.                                                                                                                                         |                                       |
      +-----------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------+
      | Processes             | Check processes on your containers and find abnormal processes.                                                                                                                                                                                                                                                     | Automatic check every hour            |
      |                       |                                                                                                                                                                                                                                                                                                                     |                                       |
      |                       | You can easily identify abnormal processes on your containers based process paths, server names, IP addresses, startup parameters, startup time, users who run the processes, file permissions, PIDs, and file hashes.                                                                                              |                                       |
      |                       |                                                                                                                                                                                                                                                                                                                     |                                       |
      |                       | If a suspicious process has not been detected in the last 30 days, its information will be automatically deleted from the process list.                                                                                                                                                                             |                                       |
      +-----------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------+
      | Installed Software    | Check and manage all software installed on your containers, and identify insecure versions.                                                                                                                                                                                                                         | Automatic check every day             |
      |                       |                                                                                                                                                                                                                                                                                                                     |                                       |
      |                       | You can check real-time and historical software information to determine whether the software is risky.                                                                                                                                                                                                             |                                       |
      |                       |                                                                                                                                                                                                                                                                                                                     |                                       |
      |                       | -  Real-time software information includes the software name, number of servers, server names, IP addresses, software versions, software update time, and the last scan time.                                                                                                                                       |                                       |
      |                       | -  Historical software change records include the server names, IP addresses, change statuses, software versions, software update time, and the last scan time.                                                                                                                                                     |                                       |
      +-----------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------+
      | Auto-startup          | Check for auto-started items and quickly locate Trojans.                                                                                                                                                                                                                                                            | Automatic check every hour            |
      |                       |                                                                                                                                                                                                                                                                                                                     |                                       |
      |                       | Real-time information about auto-started items includes their names, types (auto-started service, startup folder, pre-loaded dynamic library, Run registry key, or scheduled task), number of servers, server names, IP addresses, paths, file hashes, users, container name, container ID, and the last scan time. |                                       |
      +-----------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------+
      | Websites              | You can check statistics about web directories and sites that can be accessed from the Internet. You can view the directories and permissions, access paths, external ports, certificate information (to be provided later), and key processes of websites.                                                         | Once a week (04:10 a.m. every Monday) |
      +-----------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------+
      | Web Framework         | You can check statistics about frameworks used for web content presentation, including their versions, paths, and associated processes.                                                                                                                                                                             | Once a week (04:10 a.m. every Monday) |
      +-----------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------+
      | Middleware            | You can also check information about servers, versions, paths, and processes associated with middleware.                                                                                                                                                                                                            | Once a week (04:10 a.m. every Monday) |
      +-----------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------+
      | Web Services          | You can check details about the software used for web content access, including versions, paths, configuration files, and associated processes of all software.                                                                                                                                                     | Once a week (04:10 a.m. every Monday) |
      +-----------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------+
      | Web Applications      | You can check details about software used for web content push and release, including versions, paths, configuration files, and associated processes of all software.                                                                                                                                               | Once a week (04:10 a.m. every Monday) |
      +-----------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------+
      | Databases             | You can check details about software that provides data storage, including versions, paths, configuration files, and associated processes of all software.                                                                                                                                                          | Once a week (04:10 a.m. every Monday) |
      +-----------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------------+

Viewing Asset Fingerprint Data of a Single Container
----------------------------------------------------

#. Log in to the management console.
#. Click |image2| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.
#. In the navigation pane, choose **Asset Management** > **Servers & Quota**. Click the **Servers** tab.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.

#. Click the name of the target server. On the server details page that is displayed, click the **Asset Fingerprints** > **Containers** tab.
#. Click a fingerprint in the fingerprint list to view its asset information. For more information, see :ref:`Table 1 <hss_01_0465__table7132214184518>`.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png
.. |image2| image:: /_static/images/en-us_image_0000001517477398.png

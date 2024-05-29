:original_name: hss_01_0376.html

.. _hss_01_0376:

Uninstalling an Agent
=====================

If you no longer need to use HSS, uninstall the agent by following the instructions provided in this section. If the agent is uninstalled, HSS will stop protecting your servers and detecting risks.

Uninstalling the Agent from a Single Server in One-Click
--------------------------------------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

#. In the navigation pane, choose **Installation & Configuration**. Click the **Agents** tab.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.


   .. figure:: /_static/images/en-us_image_0000001670681801.png
      :alt: **Figure 1** Viewing agent management

      **Figure 1** Viewing agent management

#. Click **Online** to view the list of servers where the agent has been installed. For details, see :ref:`Table 1 <hss_01_0376__table1926618704616>`.

   .. _hss_01_0376__table1926618704616:

   .. table:: **Table 1** Online agent parameters

      +-----------------------------------+---------------------------------------------+
      | Parameter                         | Description                                 |
      +===================================+=============================================+
      | Server Name/ID                    | Server name and ID                          |
      +-----------------------------------+---------------------------------------------+
      | IP Address                        | EIP or private IP address of a server       |
      +-----------------------------------+---------------------------------------------+
      | OS                                | Server OS. Its value can be:                |
      |                                   |                                             |
      |                                   | -  **Linux**                                |
      |                                   | -  **Windows**                              |
      +-----------------------------------+---------------------------------------------+
      | Agent Status                      | Agent status of a server. Its value can be: |
      |                                   |                                             |
      |                                   | -  **Online**                               |
      +-----------------------------------+---------------------------------------------+

#. Click **Uninstall Agent** in the **Operation** column of a server. In the dialog box that is displayed, confirm the uninstallation information and click **OK**.

Uninstalling the Agent from Multiple Servers in One-Click
---------------------------------------------------------

#. Log in to the management console.

#. In the navigation pane, choose **Installation & Configuration**. Click the **Agents** tab.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.


   .. figure:: /_static/images/en-us_image_0000001670681801.png
      :alt: **Figure 2** Viewing agent management

      **Figure 2** Viewing agent management

#. Click **Online** to view the list of servers where the agent has been installed. For details, see :ref:`Table 2 <hss_01_0376__hss_01_0376_table1926618704616>`.

   .. _hss_01_0376__hss_01_0376_table1926618704616:

   .. table:: **Table 2** Online agent parameters

      +-----------------------------------+---------------------------------------------+
      | Parameter                         | Description                                 |
      +===================================+=============================================+
      | Server Name/ID                    | Server name and ID                          |
      +-----------------------------------+---------------------------------------------+
      | IP Address                        | EIP or private IP address of a server       |
      +-----------------------------------+---------------------------------------------+
      | OS                                | Server OS. Its value can be:                |
      |                                   |                                             |
      |                                   | -  **Linux**                                |
      |                                   | -  **Windows**                              |
      +-----------------------------------+---------------------------------------------+
      | Agent Status                      | Agent status of a server. Its value can be: |
      |                                   |                                             |
      |                                   | -  **Online**                               |
      +-----------------------------------+---------------------------------------------+

#. Select the target servers whose agent you want to uninstall.

   .. note::

      If you check the box before **Server Name/ID**, all servers on the page will be selected.


   .. figure:: /_static/images/en-us_image_0000001622044122.png
      :alt: **Figure 3** Selecting all servers whose agent needs to be uninstalled.

      **Figure 3** Selecting all servers whose agent needs to be uninstalled.

#. Click **Uninstall Agent** above the server list. In the dialog box displayed, confirm the servers from which you want to uninstall the agent and click **OK**.

Manually Uninstalling the Agent from a Linux Server
---------------------------------------------------

#. Remotely log in to the Linux server where the agent is to be uninstalled.

   -  You can log in to the ECS management console and click **Remote Login** in the ECS list.
   -  If your server has an EIP bound, you can also use a remote management tool, such as Xftp, SecureFX, WinSCP, PuTTY, or Xshell, to log in to the server and install the agent on the server as user **root**.

#. If the agent has been installed, run the following command to uninstall it:

   .. note::

      Do not run the uninstallation command in the **/usr/local/hostguard/** directory. You can run the uninstallation command in any other directory.

   -  For EulerOS, CentOS, and Red Hat, or other OSs that support RPM installation, run the **rpm -e hostguard;** command.
   -  For Ubuntu, Debian, and other OSs that support DEB installation, run the **dpkg -P hostguard;** command.

#. Verify the uninstallation. If the **/usr/local/hostguard/** directory is not found on the Linux server, the agent has been uninstalled.

Manually Uninstalling the Agent from a Windows Server
-----------------------------------------------------

#. Remotely log in to the Windows server where the agent is to be uninstalled.

   -  You can log in to the ECS management console and click **Remote Login** in the ECS list.
   -  If an EIP has been bound to the server, you can use Windows Remote Desktop Connection or a third-party remote management tool, such as mstsc or RDP, to log in to the server and install the agent on the server as an administrator.

#. Go to **C:\\Program File\\HostGuard** on the Windows server.

3. Double-click the **unins000.exe** file to uninstall the agent.
4. In the **HostGuard Uninstall** dialog box, click **Yes** to delete HostGuard and all its components.
5. (Optional) Restart the server.

   -  If you have enabled WTP, you need to restart the server after uninstalling the agent. In the **HostGuard Uninstall** dialog box, click **Yes** to restart the server.
   -  If you have not enabled WTP, you do not need to restart the server. In the **HostGuard Uninstall** dialog box, click **No** to skip server restart.

6. If the **C:\\Program Files\\HostGuard** directory does not exist on the Windows server, the agent has been uninstalled.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

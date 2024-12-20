:original_name: hss_01_0376.html

.. _hss_01_0376:

Uninstalling the Agent
======================

If you no longer need to use HSS, uninstall the agent by following the instructions provided in this section. If the agent is uninstalled, HSS will stop protecting your servers and detecting risks.

Uninstalling the Online Agents
------------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane, choose **Installation & Configuration**. Click the **Agents** tab.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.


   .. figure:: /_static/images/en-us_image_0000002087368313.png
      :alt: **Figure 1** Viewing agent management

      **Figure 1** Viewing agent management

#. Click the value of **Servers with Agents** to view the list of servers where the agent has been installed. For details, see :ref:`Table 1 <hss_01_0376__table2827951144012>`.

   .. _hss_01_0376__table2827951144012:

   .. table:: **Table 1** Online agent parameters

      +-----------------------------------+------------------------------------------------------+
      | Parameter                         | Description                                          |
      +===================================+======================================================+
      | Server Name/ID                    | Server name and ID                                   |
      +-----------------------------------+------------------------------------------------------+
      | IP Address                        | EIP or private IP address of a server                |
      +-----------------------------------+------------------------------------------------------+
      | OS                                | Server OS. Its value can be:                         |
      |                                   |                                                      |
      |                                   | -  **Linux**                                         |
      |                                   | -  **Windows**                                       |
      +-----------------------------------+------------------------------------------------------+
      | Agent Status                      | Agent status of a server. Its value can be:          |
      |                                   |                                                      |
      |                                   | -  **Online**                                        |
      +-----------------------------------+------------------------------------------------------+
      | Agent Version                     | Version of the agent installed on the target server. |
      +-----------------------------------+------------------------------------------------------+
      | Agent Upgrade Status              | The agent upgrade status.                            |
      +-----------------------------------+------------------------------------------------------+

#. Click **Uninstall Agent** in the **Operation** column of a server. In the dialog box that is displayed, confirm the uninstallation information and click **OK**.

   If you need to uninstall the agent in batches, you can select servers and click **Uninstall Agent** above the list.

Uninstall an Offline Agent
--------------------------

-  **Uninstalling the Linux agent**

   #. Log in to the server from which you want to uninstall the agent and run the following command to switch to user root:

      **su - root**

   #. .. _hss_01_0376__hss_01_0119_li547515531414:

      In any directory, run the following command to uninstall the agent:

      .. note::

         Do not run the uninstallation command in the **/usr/local/hostguard/** directory. You can run the uninstallation command in any other directory.

      -  For EulerOS, CentOS and Red Hat, or other OSs that support RPM installation, run the **rpm -e hostguard** command.
      -  For Ubuntu and Debian OSs, or other OSs that support DEB installation, run the **dpkg -P hostguard** command.

      If information similar to the following is displayed, the agent has been successfully uninstalled. If the uninstallation fails, go to the :ref:`step 3 <hss_01_0376__hss_01_0119_li1588319685517>`.

      .. code-block::

         Stopping Hostguard...
         Hostguard stopped
         Hostguard uninstalled.

   #. .. _hss_01_0376__hss_01_0119_li1588319685517:

      (Optional) If the agent fails to be uninstalled in :ref:`step 2 <hss_01_0376__hss_01_0119_li547515531414>`, perform the following operations to uninstall the agent:

      -  For OSs that support RPM installation, such as EulerOS, CentOS, and Red Hat,

         a. Run the following command to delete the installation record:

            **rpm -e --justdb hostguard**

         b. Run the following command to check whether there are hostguard processes:

            **ps -ef \| grep hostguard**

            If there are residual processes, run the **kill -9 PID** command to stop all residual processes.

         c. Run the following command to check whether the **/usr/local/hostguard** directory exists:

            **ll /usr/local/hostguard**

            If the directory exists, run the **rm -rf /usr/local/hostguard** command to delete it.

         d. Run the following command to check whether the **/etc/init.d/hostguard** file exists:

            **ll /etc/init.d/hostguard**

            If the file exists, run the **rm -f /etc/init.d/hostguard** command to delete the file.

      -  For OSs that support DEB installation, such as Ubuntu and Debian.

         a. Run the following command to check whether there are hostguard processes:

            **ps -ef \| grep hostguard**

            If there are residual processes, run the **kill -9 PID** command to stop all residual processes.

         b. Run the following command to check whether the **/usr/local/hostguard** directory exists:

            **ll /usr/local/hostguard**

            If the directory exists, run the **rm -rf /usr/local/hostguard** command to delete it.

         c. Run the following command to check whether the **/etc/init.d/hostguard** file exists:

            **ll /etc/init.d/hostguard**

            If the file exists, run the **rm -f /etc/init.d/hostguard** command to delete the file.

-  **Uninstalling the Windows agent**

   #. Log in to the server that you want to uninstall the agent.
   #. Click **Start** and choose **Control Panel** > **Programs**. Then select **HostGuard** and click **Uninstall**.

      .. note::

         -  Alternatively, go to the **C:\\Program File\\HostGuard** directory and double-click **unins000.exe** to uninstall the program.
         -  If you have created a folder for storing the agent shortcut under the **Start** menu when installing the agent, you can also choose **Start** > **HostGuard** > **Uninstall HostGuard** to uninstall HostGuard.

   #. In the **Uninstall HostGuard** dialog box, click **Yes**.
   #. (Optional) Restart the server.

      -  If you have enabled WTP, you need to restart the server after uninstalling the agent. In the **Uninstall HostGuard** dialog box, click **Yes** to restart the server.
      -  If you have not enabled WTP, you do not need to restart the server. In the **Uninstall HostGuard** dialog box, click **No** to skip server restart.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

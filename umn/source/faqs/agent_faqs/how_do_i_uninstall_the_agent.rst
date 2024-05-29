:original_name: hss_01_0119.html

.. _hss_01_0119:

How Do I Uninstall the Agent?
=============================

Two uninstallation methods are available: one-click uninstallation and manual local uninstallation.

Scenario
--------

-  The agent was installed using an incorrect package and you need to uninstall it.
-  The agent was installed using incorrect commands and you need to uninstall it.
-  If the agent fails to be upgraded, uninstall the agent.

Prerequisites
-------------

When you uninstall the agent on the management console, the **Agent Status** of the server is **Online**.

Uninstalling the Agent on the Console in One-Click
--------------------------------------------------

You can uninstall an HSS agent from the HSS console.

.. note::

   After the agent is uninstalled from a server, HSS will not provide any protection for the server.

#. Log in to the management console.

#. In the navigation pane, choose **Installation and Configuration**.

#. On the displayed page, click the **Agents** tab and click **Online**. In the row containing the desired server, click **Uninstall Agent** in the **Operation** column.

#. In the displayed dialog box, click **OK**.

   In the server list, if **Agent Status** of the server is **Offline**, its agent is successfully uninstalled.

Uninstalling the Agent from the Server
--------------------------------------

You can manually uninstall an agent on a server when you no longer use HSS or need to reinstall the agent.

.. note::

   After the agent is uninstalled from the target server, HSS will not provide any protection for the server.

-  **Uninstalling the Linux agent**

   #. Log in to the server from which you want to uninstall the agent and run the following command to switch to user root:

      **su - root**

   #. .. _hss_01_0119__li547515531414:

      In any directory, run the following command to uninstall the agent:

      .. note::

         Do not run the uninstallation command in the **/usr/local/hostguard/** directory. You can run the uninstallation command in any other directory.

      -  For EulerOS, CentOS and Red Hat, or other OSs that support RPM installation, run the **rpm -e hostguard** command.
      -  For Ubuntu and Debian OSs, or other OSs that support DEB installation, run the **dpkg -P hostguard** command.

      If information similar to the following is displayed, the agent has been successfully uninstalled. If the uninstallation fails, go to the :ref:`step 3 <hss_01_0119__li1588319685517>`.

      .. code-block::

         Stopping Hostguard...
         Hostguard stopped
         Hostguard uninstalled.

   #. .. _hss_01_0119__li1588319685517:

      (Optional) If the agent fails to be uninstalled in :ref:`step 2 <hss_01_0119__li547515531414>`, perform the following operations to uninstall the agent:

      -  For OSs that support RPM installation, such as EulerOS, CentOS, and Red Hat.

         a. Run the following command to delete the installation record:

            **rpm -e --justdb hostguard**

         b. Run the following command to check whether there are hostguard processes:

            **ps -ef \| grep hostguard**

            If there are residual processes, run the **kill -9 PID** command to kill all residual processes.

         c. Run the following command to check whether the **/usr/local/hostguard** directory exists:

            **ll /usr/local/hostguard**

            If the directory exists, run the **rm -rf /usr/local/hostguard** command to delete it.

         d. Run the following command to check whether the **/etc/init.d/hostguard** file exists:

            **ll /etc/init.d/hostguard**

            If the file exists, run the **rm -f /etc/init.d/hostguard** command to delete the file.

      -  For OSs that support DEB installation, such as Ubuntu and Debian.

         a. Run the following command to check whether there are hostguard processes:

            **ps -ef \| grep hostguard**

            If there are residual processes, run the **kill -9 PID** command to kill all residual processes.

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

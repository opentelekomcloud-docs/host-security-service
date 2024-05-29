:original_name: hss_01_0472.html

.. _hss_01_0472:

How Do I Disable the SELinux Firewall?
======================================

Security-Enhanced Linux (SELinux) is a kernel module and security subsystem of Linux.

SELinux minimizes the resources that can be accessed by service processes in the system (the principle of least privilege).

Closure Description
-------------------

-  After the SELinux is disabled, services are not affected.
-  SELinux can be disabled temporarily or permanently as required.

Scenario
--------

To use the two-factor authentication function of HSS, you need to permanently disable the SELinux firewall.

Procedure
---------

#. Remotely log in to the destination server.

   You can log in to the ECS management console and click **Remote Login** in the ECS list.

   If your server has an EIP bound, you can also use a remote management tool, such as PuTTY or Xshell, to log in to the server and install the agent on the server as user **root**.

#. Run the shutdown command in the command window.

   -  **Temporarily disable SELinux**

      Run the following command in the CLI to temporarily disable SELinux:

      .. code-block::

         setenforce 0

      .. note::

         After the system is restarted, the SELinux will be enabled again.

   -  **Permanently disable SELinux**

      a. Run the following command in the directory window to edit the **config** file of SELinux:

         .. code-block::

            vi /etc/selinux/config

      b. Locate **SELINUX=enforcing**, press **i** to enter the editing mode, and change the parameter to **SELINUX=disabled**.


         .. figure:: /_static/images/en-us_image_0000001568637593.png
            :alt: **Figure 1** Editing the SELinux status

            **Figure 1** Editing the SELinux status

      c. After the modification, press **Esc** and run the following command to save the file and exit:

         .. code-block::

            :wq

#. Run the permanent shutdown command, save the settings, and exit. Run the following command to restart the server immediately:

   .. code-block::

      shutdown -r now

   .. note::

      The permanent shutdown command takes effect only after the server is restarted.

#. After the restart, run the following command to verify that SELinux is disabled:

   .. code-block::

      getenforce

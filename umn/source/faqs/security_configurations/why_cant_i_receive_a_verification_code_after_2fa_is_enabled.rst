:original_name: hss_01_0439.html

.. _hss_01_0439:

Why Can't I Receive a Verification Code After 2FA Is Enabled?
=============================================================

-  The two-factor authentication function does not take effect immediately after being enabled.

   Wait for 5 minutes and try again.

-  To enable two-factor authentication, you need to disable the SELinux firewall.

   :ref:`Disable the SELinux firewall <hss_01_0472>` and try again.

-  Linux servers require user passwords for login.

   To switch from the key login mode to password login mode, perform the following steps:

   #. Use the key to log in to the Linux ECS and set the password of user **root**.

      **sudo passwd root**

      If the key file is lost or damaged, reset the password of user **root**.

   #. Modify the SSH configuration file on the ECS as user **root**.

      **su root**

      **vi /etc/ssh/sshd_config**

      Modify the following settings:

      -  Change **PasswordAuthentication no** to **PasswordAuthentication yes**.

         Alternatively, delete the comment tag (#) before **PasswordAuthentication yes**.

      -  Change **PermitRootLogin no** to **PermitRootLogin yes**.

         Alternatively, delete the comment tag (#) before **PermitRootLogin yes**.

   #. Restart sshd for the modification to take effect.

      **service sshd restart**

   #. Restart the ECS. Then, you can log in to the ECS as user **root** using the password.

      .. note::

         To prevent unauthorized users from using the key file to access the Linux ECS, delete the **/root/.ssh/authorized_keys** file or clear the **authorized_keys** file.

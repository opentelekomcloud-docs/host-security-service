:original_name: hss_01_0440.html

.. _hss_01_0440:

Why Does My Login Fail After I Enable 2FA?
==========================================

The login failed probably because file configurations or the login mode was incorrect.

Correcting File Configurations
------------------------------

Check whether the configuration file is correct.

Configuration file path: **/etc/ssh/sshd_config**

Configuration items:

PermitEmptyPasswords no

UsePAM yes

ChallengeResponseAuthentication yes

.. important::

   If you use the **root** account for login,the following configuration item is required:

   PermitRootLogin yes

Correcting the Login Mode
-------------------------

If you attempted to log in in either of the following ways, your login would fail.

-  Used CloudShell to log in to an ECS.
-  Attempted to log in to a Linux server through a CBH instance.

Failure cause: 2FA is implemented through a built-in module, which cannot be displayed if you log in in the preceding ways. As a result, the login authentication fails.

Solution: Perform login authentication by referring to :ref:`How Do I Use 2FA? <hss_01_0437>`

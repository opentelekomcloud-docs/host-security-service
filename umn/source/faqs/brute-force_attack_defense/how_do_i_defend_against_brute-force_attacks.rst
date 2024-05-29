:original_name: hss_01_0256.html

.. _hss_01_0256:

How Do I Defend Against Brute-force Attacks?
============================================

Impact of Account Cracking
--------------------------

Intruders who cracked server accounts can exploit permissions to steal or tamper with data on servers, interrupting enterprise services and causing great loss.

Preventive Measures
-------------------

-  Configure the SSH login whitelist.

   The SSH login whitelist allows logins from only whitelisted IP address, effectively preventing account cracking.

-  Enable 2FA.

   2FA requires users to provide verification codes before they log in. The codes will be sent to their mobile phones or email boxes.

   Choose **Installation & Configuration**. On the **Two-Factor Authentication** tab, select servers and click **Enable 2FA**.

-  Use non-default ports.

   Change the default remote management ports 22 and 3389 to other ports.

-  Configure security group rules to prevent the attacking IP addresses from accessing your service ports.

   .. note::

      You are advised to allow only specified IP addresses to access open remote management ports (for example, for SSH and remote desktop login).

   You can configure security group rules to control access to your servers. For a port used for remote login, you can set IP addresses that are allowed to remotely log in to your ECSs.

   To allow IP address **192.168.20.2** to remotely access Linux ECSs in a security group over the SSH protocol and port 22, you can configure the following security group rule.

   .. table:: **Table 1** Setting IP addresses to remotely connect to ECSs

      ========= ==================== ==== ============================
      Direction Protocol/Application Port Source
      ========= ==================== ==== ============================
      Inbound   SSH (22)             22   For example, 192.168.20.2/32
      ========= ==================== ==== ============================

-  Set a strong password.

   HSS baseline checks include the password policy check and weak password detection, which can find accounts that use weak passwords on your servers. You can view and handle password risks on the console.

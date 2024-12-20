:original_name: hss_01_0568.html

.. _hss_01_0568:

Enabling 2FA
============

Two-factor authentication (2FA) requires users to provide verification codes before they log in. The codes will be sent to their mobile phones or email boxes. You have to choose an SMN topic for servers where 2FA is enabled. The topic specifies the recipients of login verification codes, and HSS will authenticate login users accordingly.

Prerequisites
-------------

-  You have created a message topic and added a subscription. For details, see "Creating a Topic" and "Adding Subscriptions" in *Simple Message Notification User Guide*.
-  Server protection has been enabled. For details, see :ref:`Enabling Protection <hss_01_0260>`.
-  To enable 2FA, you need to disable the SELinux firewall.

Constraints and Limitations
---------------------------

-  If 2FA is enabled, it can be used only in following scenarios:

   -  Linux: The SSH password is used to log in to an ECS, and the OpenSSH version is earlier than 8.
   -  Windows: The RDP file is used to log in to a Windows ECS.

-  When two-factor authentication is enabled for Windows ECSs, the **User must change password at next logon** function is not allowed. To use this function, disable two-factor authentication.


Enabling 2FA
------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. Choose **Installation & Configuration** > **Two-Factor Authentication**.

#. Select servers and click **Enable 2FA** above the list, or select a server and click **Enable 2FA** in the **Operation** column.


   .. figure:: /_static/images/en-us_image_0000002087636653.png
      :alt: **Figure 1** Enabling 2FA

      **Figure 1** Enabling 2FA

#. In the displayed **Enable 2FA** dialog box, select an authentication mode.

   -  **SMS/Email**

      You need to select an SMN topic for SMS and email verification.

      -  The drop-down list displays only notification topics that have been confirmed.
      -  If there is no topic, click **View** to create one.
      -  During authentication, all the mobile numbers and email addresses specified in the topic will receive a verification SMS or email. You can delete mobile numbers and email addresses that do not need to receive verification messages.


      .. figure:: /_static/images/en-us_image_0000001908433517.png
         :alt: **Figure 2** SMS/Email verification

         **Figure 2** SMS/Email verification

   -  **Verification code**

      Use the verification code you receive in real time for verification.


      .. figure:: /_static/images/en-us_image_0000001862553600.png
         :alt: **Figure 3** Verification code

         **Figure 3** Verification code

#. Click **OK**. After 2FA is enabled, it takes about 5 minutes for the configuration to take effect.

   .. important::

      When you log in to a remote Windows server from another Windows server where 2FA is enabled, you need to manually add credentials on the latter. Otherwise, the login will fail.

      To add credentials, choose **Start** > **Control Panel**, and click **User Accounts**. Click **Manage your credentials** and then click **Add a Windows credential**. Add the username and password of the remote server that you want to access.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

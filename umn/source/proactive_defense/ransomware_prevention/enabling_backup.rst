:original_name: hss_01_0562.html

.. _hss_01_0562:

Enabling Backup
===============

To enhance defense and reduce service loss caused by ransomware attacks, you are advised to periodically back up data on servers.

Enabling Ransomware Backup
--------------------------

#. Log in to the management console.
#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.
#. Choose **Prevention** > **Ransomware Prevention**.

   .. note::

      If your servers are managed by enterprise projects, you can select the target enterprise project to view or operate the asset and detection information.

#. Click the **Protected Servers** tab.
#. Select a server and click **Enable Backup**.
#. In the **Enable Backup** dialog box, select a vault.

   .. note::

      A vault that meets the following conditions can be bound:

      -  The vault is in **Available** or **Locked** state.
      -  The backup policy is in **Enabled** state.
      -  The vault has backup capacity available.
      -  The vault is bound to fewer than 256 servers.

#. Click **OK**.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

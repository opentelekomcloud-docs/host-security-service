:original_name: hss_01_0397.html

.. _hss_01_0397:

Enabling the Enterprise/Premium Edition
=======================================

Before enabling protection on servers, you need to allocate quota to a specified server. If the protection is disabled or the server is deleted, the quota can be allocated to other servers.

For the WTP edition, choose **Prevention** > **Web Tamper Protection** > **Server Protection** and then enable it.

.. note::

   To enable the WTP edition, choose **Prevention** > **Web Tamper Protection** > **Server Protection** and click the **Servers** tab. All the functions of the premium edition are included with the WTP edition.

Check Mode
----------

HSS performs a full scan in the early morning every day.

After you enable server protection, you can view scan results after the automatic scan in the next early morning.

Prerequisites
-------------

-  The agent has been installed on the servers to be protected, the agent status is **Online**, and the protection status is **Unprotected**.

-  To better protect your containers, you are advised to set security configurations.

Restrictions
------------

Windows

-  Authorize the Windows firewall when you enable protection for a Windows server. Do not disable the Windows firewall during the HSS in-service period. If the Windows firewall is disabled, HSS cannot block brute-force attack IP addresses.
-  If the Windows firewall is manually enabled, HSS may also fail to block brute-force attack IP addresses.

Enabling Protection
-------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane, choose **Asset Management** > **Servers & Quota**. Click the **Servers** tab.


   .. figure:: /_static/images/en-us_image_0000001801549361.png
      :alt: **Figure 1** Server list

      **Figure 1** Server list

#. Select the target server and click **Enable**.

   In the **Enable Protection** dialog box, select an HSS edition.


   .. figure:: /_static/images/en-us_image_0000001629357728.png
      :alt: **Figure 2** Enabling HSS

      **Figure 2** Enabling HSS


   .. figure:: /_static/images/en-us_image_0000001563224758.png
      :alt: **Figure 3** Confirming the protection information

      **Figure 3** Confirming the protection information

#. Click **OK**. View the server protection status in the server list.

   If the **Protection Status** of the target server is **Enabled**, the enterprise or premium edition has been enabled.

   .. note::

      -  A quota can be bound to a server to protect it, on condition that the agent on the server is online.

   After HSS is enabled, it will scan your servers for security issues. Check items vary according to the edition you enabled.

Viewing Detection Details
-------------------------

After server protection is enabled, HSS will immediately perform comprehensive detection on the server. The detection may take a long time.

On the left of the protection list, click **Risky**.


.. figure:: /_static/images/en-us_image_0000002086995685.png
   :alt: **Figure 4** Viewing risky items

   **Figure 4** Viewing risky items

Click a server name to go to the details page. On this page, you can quickly check the detected information and risks of the server.


.. figure:: /_static/images/en-us_image_0000002087652133.png
   :alt: **Figure 5** Viewing the detection result

   **Figure 5** Viewing the detection result

Follow-up Procedure
-------------------

You can manually configure check items. Configurable items vary according to the edition you enabled.


.. figure:: /_static/images/en-us_image_0000001558495162.png
   :alt: **Figure 6** Manual check items

   **Figure 6** Manual check items

.. table:: **Table 1** Manual check items

   +-------------------------+----------------------------------------+----------------------------------------------------+
   | Function                | Check Item                             | Reference                                          |
   +=========================+========================================+====================================================+
   | Security Configurations | -  Common login location/IP address    | :ref:`Common Security Configuration <hss_01_0051>` |
   |                         | -  SSH login IP address whitelist      |                                                    |
   |                         | -  Isolate and kill malicious programs |                                                    |
   +-------------------------+----------------------------------------+----------------------------------------------------+
   | Intrusion Detection     | -  Alarm whitelist                     | :ref:`Intrusion Detection <hss_01_0030>`           |
   |                         | -  Login Whitelist configuration       |                                                    |
   +-------------------------+----------------------------------------+----------------------------------------------------+
   | Prevention              | -  Application protection              | :ref:`Proactive Defense <hss_01_0142>`             |
   |                         | -  Ransomware prevention               |                                                    |
   |                         | -  File integrity monitoring (FIM)     |                                                    |
   +-------------------------+----------------------------------------+----------------------------------------------------+

Related Operations
------------------

**Disabling HSS**

On the **Servers** tab of the **Servers & Quotas** page, click **Disable** in the **Operation** column of a server.

.. important::

   -  Before disabling protection, perform a comprehensive detection on the server, handle known risks, and record operation information to prevent attacks.
   -  After protection is disabled, clear important data on the server, stop important applications on the server, and disconnect the server from the external network to avoid unnecessary loss caused by attacks.

**Unbinding quota**

Choose **Asset Management** > **Servers & Quota**, and click the **Quotas** tab. Click **Unbind** in the **Operation** column. The usage status of the unbound quota will change from **In use** to **Idle**. HSS will automatically disable protection for the server unbound from the quota.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

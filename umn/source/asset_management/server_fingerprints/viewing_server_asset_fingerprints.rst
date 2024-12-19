:original_name: hss_01_0383.html

.. _hss_01_0383:

Viewing Server Asset Fingerprints
=================================

HSS can collect server asset fingerprints, including information about ports, processes, web applications, web services, web frameworks, and auto-started items. You can centrally check server asset information and detect risky assets in a timely manner based on the server fingerprints.

This section describes how to view the collected server asset fingerprints on the console. For more information, see :ref:`Collecting Server Asset Fingerprints <hss_01_0477>`.

Viewing Asset Information of All Servers
----------------------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. Choose **Asset Management** > **Server Fingerprints** to view all server assets.

   .. note::

      If your servers are managed by enterprise projects, you can select the target enterprise project to view or operate the asset and detection information.


   .. figure:: /_static/images/en-us_image_0000001853711513.png
      :alt: **Figure 1** Viewing server asset information

      **Figure 1** Viewing server asset information

#. Click a fingerprint type in the list to view the asset information.

#. (Optional) Remove risky assets.

   If you find unsafe assets after counting, remove them in a timely manner.

   You are advised to handle unsafe ports as follows:

   -  If HSS detects open high-risk ports or unused ports, check whether they are really used by your services. If they are not, disable them. For dangerous ports, you are advised to further check their program files, and delete or isolate their source files if necessary.
   -  If a detected high-risk port is actually a normal port used for services, you can ignore it. Ignored alarms will neither be recorded as unsafe items and nor trigger alarms.

Viewing Asset Information of a Single Server
--------------------------------------------

#. Log in to the management console.

#. Click |image2| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane, choose **Asset Management** > **Servers & Quota**. Click the **Servers** tab.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.

#. Click the name of the target server. On the server details page that is displayed, choose **Asset Fingerprints** > **Servers**.

#. Click a fingerprint type in the list to view the asset information.

#. (Optional) Remove risky assets.

   If you find unsafe assets after counting, remove them in a timely manner.

   You are advised to handle unsafe ports as follows:

   -  If HSS detects open high-risk ports or unused ports, check whether they are really used by your services. If they are not, disable them. For dangerous ports, you are advised to further check their program files, and delete or isolate their source files if necessary.
   -  If a detected high-risk port is actually a normal port used for services, you can ignore it. Ignored alarms will neither be recorded as unsafe items and nor trigger alarms.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png
.. |image2| image:: /_static/images/en-us_image_0000001517477398.png

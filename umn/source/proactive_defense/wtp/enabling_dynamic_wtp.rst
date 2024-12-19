:original_name: hss_01_0218.html

.. _hss_01_0218:

Enabling Dynamic WTP
====================

Dynamic WTP protects your web pages while Tomcat applications are running, and can detect tampering of dynamic data, such as database data. It can be enabled with static WTP or separately.

Constraints and Limitations
---------------------------

-  Only the servers that are protected by the HSS WTP edition support the operations described in this section.

-  Dynamic WTP can be provided only for Tomcat running JDK 8.

Prerequisites
-------------

You are using a server running the Linux OS.


Enabling Dynamic WTP
--------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. Choose **Prevention** > **Web Tamper Protection**. Click **Configure Protection** in the **Operation** column.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.


   .. figure:: /_static/images/en-us_image_0000001854854673.png
      :alt: **Figure 1** Entering the page of protection settings

      **Figure 1** Entering the page of protection settings

#. On the **Configure Protection** tab, toggle on |image2| to enable **Dynamic WTP**.


   .. figure:: /_static/images/en-us_image_0000001621322446.png
      :alt: **Figure 2** Enabling Dynamic WTP

      **Figure 2** Enabling Dynamic WTP

#. In the displayed dialog box, modify the **Tomcat bin Directory**.

   To enable dynamic WTP, you need to modify the Tomcat bin directory first. The system presets the **setenv.sh** script in the bin directory for setting anti-tamper program startup parameters. After enabling dynamic WTP, restart Tomcat to make this setting take effect.


   .. figure:: /_static/images/en-us_image_0000001669602353.png
      :alt: **Figure 3** Configuring a Tomcat directory

      **Figure 3** Configuring a Tomcat directory

#. Click **OK** to enable dynamic WTP.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png
.. |image2| image:: /_static/images/en-us_image_0000001517637478.png

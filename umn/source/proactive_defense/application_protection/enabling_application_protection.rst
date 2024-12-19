:original_name: hss_01_0390.html

.. _hss_01_0390:

Enabling Application Protection
===============================

Scenario
--------

To protect Java applications on Linux servers, enable application protection for the servers. HSS will install the RASP plug-in on the servers, and you will need to configure startup parameters.


Enabling Application Protection
-------------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. Choose **Prevention** > **Application Protection**. Click the **Protected Servers** tab.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.


   .. figure:: /_static/images/en-us_image_0000002051045448.png
      :alt: **Figure 1** Viewing protection settings

      **Figure 1** Viewing protection settings

#. Click **Add Server**. Select servers in the dialog box that is displayed.

   .. note::

      You can select a default security policy or create a security policy.


   .. figure:: /_static/images/en-us_image_0000001669828885.png
      :alt: **Figure 2** Selecting the target server and policy

      **Figure 2** Selecting the target server and policy

#. Click **Add and Enable Protection**.

#. On the **Protected Servers** tab, click the status in the **RASP Protection** column.

#. Check the RASP software installation progress. Wait until the message "Installation completed." is displayed.

#. Log in to the server, go to the Spring Boot startup path, and copy the parameters from the **Configure Startup Parameters** step to the command box.

#. Restart the microservice to apply the protection settings.

#. On the **Protected Servers** tab, check the protection status in the **Microservice Protection** column. If the status is **Active**, the protection has been enabled.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

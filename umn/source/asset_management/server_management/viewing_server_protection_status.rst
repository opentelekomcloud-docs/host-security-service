:original_name: hss_01_0003.html

.. _hss_01_0003:

Viewing Server Protection Status
================================

The server list on the **Servers** page displays the protection status of only the servers used in the selected region.


Viewing Server Protection Status
--------------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > . The page is displayed.

#. In the navigation pane, choose **Asset Management** > **Servers & Quota**. On the **Servers** tab, view the protection status of the server. For more information, see :ref:`Table 1 <hss_01_0003__table10943651111514>`.

   .. note::

      If your servers are managed by enterprise projects, you can select the target enterprise project to view or operate the asset and detection information.


   .. figure:: /_static/images/en-us_image_0000001830849746.png
      :alt: **Figure 1** Server protection status

      **Figure 1** Server protection status

   -  To check the protection status of a server, enter a server name, server ID, or IP address in the search box above the server protection list.
   -  On the left of the server protection list, select a server protection edition or an asset importance category to view the protection status of each type of servers.

   .. _hss_01_0003__table10943651111514:

   .. table:: **Table 1** Protection status description

      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                          |
      +===================================+======================================================================================================================================================+
      | Agent Status                      | -  **Not installed**: The agent has not been installed or successfully started.                                                                      |
      |                                   |                                                                                                                                                      |
      |                                   |    Click **Install Agent** and install the agent as prompted.                                                                                        |
      |                                   |                                                                                                                                                      |
      |                                   | -  **Online**: The agent is running properly.                                                                                                        |
      |                                   |                                                                                                                                                      |
      |                                   | -  **Offline**: The communication between the agent and the HSS server is abnormal, and HSS cannot protect your servers.                             |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Protection Status                 | -  **Enabled**: The server is fully protected by HSS.                                                                                                |
      |                                   | -  **Unprotected**: HSS is disabled for the server. After the agent is installed, click **Enable** in the **Operation** column to enable protection. |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Scan Results                      | -  **Risky**: The host has risks.                                                                                                                    |
      |                                   | -  **Safe**: No risks are found.                                                                                                                     |
      |                                   | -  **Pending risk detection**: HSS is not enabled for the server.                                                                                    |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+

Viewing the WTP Status
----------------------

#. Log in to the management console and go to the HSS page.

#. Choose **Prevention** > **Web Tamper Protection** and click **Servers** to view the protection status of the servers.

   To check the protection status of a target server, enter a server name, server ID, or IP address in the search box above the protection list, and click |image2|.


   .. figure:: /_static/images/en-us_image_0000001757768557.png
      :alt: **Figure 2** Servers protected by WTP

      **Figure 2** Servers protected by WTP

   .. table:: **Table 2** Statuses

      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                        |
      +===================================+====================================================================================================================+
      | Protection Status                 | **Protected**: HSS provides static web tamper protection (WTP) for the server.                                     |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------+
      | Dynamic WTP                       | Status of dynamic WTP, which can be:                                                                               |
      |                                   |                                                                                                                    |
      |                                   | -  |image3|: Dynamic WTP is enabled.                                                                               |
      |                                   | -  |image4|: Dynamic WTP is disabled. After enabling dynamic WTP, restart Tomcat to make this setting take effect. |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------+
      | Static Tampering Attacks          | Number of times that static web page files are attacked and tampered with.                                         |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------+
      | Dynamic Tampering Attacks         | Number of web application vulnerability exploits and injection attacks.                                            |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------+

Exporting the Server List
-------------------------

#. Log in to the management console and go to the HSS page.

#. Choose **Asset Management** > **Servers & Quota**. The **Servers** tab page is displayed.

#. Click |image5| in the upper right corner of the **Server** tab page to export the details of the server list.

   .. note::

      The details of up to 1000 servers can be exported at a time.


   .. figure:: /_static/images/en-us_image_0000001735544818.png
      :alt: **Figure 3** Exporting the server list

      **Figure 3** Exporting the server list

.. |image1| image:: /_static/images/en-us_image_0000001703888418.png
.. |image2| image:: /_static/images/en-us_image_0000001630021161.png
.. |image3| image:: /_static/images/en-us_image_0000001606964064.png
.. |image4| image:: /_static/images/en-us_image_0000001606804308.png
.. |image5| image:: /_static/images/en-us_image_0000001568437401.png

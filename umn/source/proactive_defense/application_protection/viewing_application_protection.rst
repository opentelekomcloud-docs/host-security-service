:original_name: hss_01_0389.html

.. _hss_01_0389:

Viewing Application Protection
==============================

Scenario
--------

After application protection is enabled, you can view the protection status and events on the **Application Protection** page. You can analyze the events and harden your applications accordingly.

Viewing the Protection Status
-----------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. Choose **Prevention** > **Application Protection**. Click the **Protected Servers** tab.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.


   .. figure:: /_static/images/en-us_image_0000002051045448.png
      :alt: **Figure 1** Viewing protection settings

      **Figure 1** Viewing protection settings

#. View the service protection status. For details, see :ref:`Table 1 <hss_01_0389__table162143211567>`.

   .. _hss_01_0389__table162143211567:

   .. table:: **Table 1** Parameters for protection settings

      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                                                                          |
      +===================================+======================================================================================================================================================================================================================+
      | Server Name/ID                    | Server name and ID                                                                                                                                                                                                   |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | IP Address                        | Private IP address and EIP of the server                                                                                                                                                                             |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | OS                                | Server OS                                                                                                                                                                                                            |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Server Group                      | Group that the server belongs to                                                                                                                                                                                     |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Policy                            | Detection policies bound to the target server.                                                                                                                                                                       |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Protection Status                 | Agent status of a server.                                                                                                                                                                                            |
      |                                   |                                                                                                                                                                                                                      |
      |                                   | -  Protected: The agent is online.                                                                                                                                                                                   |
      |                                   | -  Unprotected: The agent is offline.                                                                                                                                                                                |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Microservice Protection           | Microservice protection status. Its value can be:                                                                                                                                                                    |
      |                                   |                                                                                                                                                                                                                      |
      |                                   | -  Effective: The microservice protection is enabled successfully.                                                                                                                                                   |
      |                                   | -  Installing: The microservice RASP protection software is being installed and protection is disabled.                                                                                                              |
      |                                   | -  Installed but not configured: The microservice RASP protection software is successfully installed, but microservice startup parameters are not configured and protection is disabled.                             |
      |                                   | -  Installation failed: The microservice RASP protection software fails to be installed.                                                                                                                             |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | RASP Protection.                  | RASP protection status. Its value can be:                                                                                                                                                                            |
      |                                   |                                                                                                                                                                                                                      |
      |                                   | If the following information is displayed next to |image2|, protection is not enabled. Check whether there are operations that are not handled by referring to :ref:`Enabling Application Protection <hss_01_0390>`. |
      |                                   |                                                                                                                                                                                                                      |
      |                                   | -  Installing: The microservice RASP protection software is being installed and protection is disabled.                                                                                                              |
      |                                   | -  Installed but not configured: The microservice RASP protection software is successfully installed, but microservice startup parameters are not configured and protection is disabled.                             |
      |                                   | -  Installation failed: The microservice RASP protection software fails to be installed.                                                                                                                             |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Detected Attacks                  | Number of attacks detected by RASP.                                                                                                                                                                                  |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Viewing Events
--------------

#. Log in to the management console and go to the HSS page.

#. Choose **Prevention** > **Application Protection** and click the **Events** tab. For more information, see :ref:`Table 2 <hss_01_0389__table1953772412357>`.


   .. figure:: /_static/images/en-us_image_0000001854003221.png
      :alt: **Figure 2** Viewing protection events

      **Figure 2** Viewing protection events

   .. _hss_01_0389__table1953772412357:

   .. table:: **Table 2** Event parameters

      +-----------------------------------+-----------------------------------------------------------------+
      | Parameter                         | Description                                                     |
      +===================================+=================================================================+
      | Severity                          | Alarm severity. You can search for servers by alarm severities. |
      |                                   |                                                                 |
      |                                   | -  **Critical**                                                 |
      |                                   | -  **High**                                                     |
      |                                   | -  **Medium**                                                   |
      |                                   | -  **Low**                                                      |
      +-----------------------------------+-----------------------------------------------------------------+
      | Server Name                       | Server that triggers an alarm                                   |
      +-----------------------------------+-----------------------------------------------------------------+
      | Alarm Name                        | Alarm name                                                      |
      +-----------------------------------+-----------------------------------------------------------------+
      | Alarm Time                        | Time when an alarm is reported                                  |
      +-----------------------------------+-----------------------------------------------------------------+
      | Attack Source IP Address          | IP address of the server that triggers the alarm                |
      +-----------------------------------+-----------------------------------------------------------------+
      | Attack Source URL                 | URL of the server that triggers the alarm                       |
      +-----------------------------------+-----------------------------------------------------------------+

#. You can click an alarm name to view the attack information (such as the request information and attack source IP address) and extended information (such as detection rule ID and description), and troubleshoot the problem accordingly.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png
.. |image2| image:: /_static/images/en-us_image_0000001807123476.png

:original_name: hss_01_0600.html

.. _hss_01_0600:

Creating a Protection Policy for a Dynamic Honeypot Port
========================================================

Scenario
--------

The dynamic port honeypot function uses a real port as a honeypot port to induce attackers to access the network. Therefore, when enabling dynamic port honeypot protection, you need to create a protection policy to add a server port as a honeypot port and bind it to the server for protection.

This chapter describes how to create a dynamic port honeypot protection policy.

Constraints and Limitations
---------------------------

-  A maximum of 10 honeypot ports can be added to a server.
-  A honeypot port can be bound to only one protocol. Both TCP and TCP6 are supported.


Creating a Protection Policy for a Dynamic Honeypot Port
--------------------------------------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. Choose **Prevention** > **Dynamic Port Honeypot**.

#. On the **Servers** tab, click **Create a Protection Policy**. The dialog box is displayed.

#. Create a protection policy as prompted.

   a. .. _hss_01_0600__li41374502470:

      Configure the policy and click **Next**. For details about related parameters, see :ref:`Table 1 <hss_01_0600__table3740181655011>`

      .. _hss_01_0600__table3740181655011:

      .. table:: **Table 1** Parameters for creating a protection policy

         +----------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
         | Parameter                              | Description                                                                                                                                                                              |
         +========================================+==========================================================================================================================================================================================+
         | Policy Name                            | You can retain the default name or enter a name that is easy to identify.                                                                                                                |
         +----------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
         | OS Type                                | Select an OS type of a server to which you want to add the dynamic port honeypot function.                                                                                               |
         +----------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
         | Protected Port                         | Select a server port that implements the dynamic port honeypot function.                                                                                                                 |
         |                                        |                                                                                                                                                                                          |
         |                                        | -  **Recommended Port**: For Linux, common Windows ports are recommended. For Windows, common Linux ports are recommended.                                                               |
         |                                        | -  **Custom Port**: You can add custom ports or delete some recommended ports as required.                                                                                               |
         |                                        |                                                                                                                                                                                          |
         |                                        | .. note::                                                                                                                                                                                |
         |                                        |                                                                                                                                                                                          |
         |                                        |    Ensure that the port to be added is not occupied by other services. If the port is occupied, the dynamic port honeypot function fails to be enabled.                                  |
         +----------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
         | (Optional) Source IP address whitelist | By default, the servers that proactively connect to the dynamic honeypot port are compromised intranet servers. Once a suspicious connection behavior is detected, an alarm is reported. |
         |                                        |                                                                                                                                                                                          |
         |                                        | Therefore, if a trusted server may connect to the port, you are advised to add the IP address to the source IP address whitelist.                                                        |
         +----------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

   b. Select the target server and click **Save and Enable**.

      Note that the dynamic port honeypot can be selected only for the servers that meet all the following conditions:

      -  The HSS premium edition or higher has been enabled on the server.
      -  The server agent is online. The Windows agent version is 4.0.22 or later, and the Linux agent version is 3.2.10 or later.
      -  No dynamic port honeypot policies have been bound to the server.
      -  The OS type of the server is the same as that specified in :ref:`5.a <hss_01_0600__li41374502470>`.
      -  No EIPs have been bound to the server.

#. In the **Associated Servers** column of the created target policy, click the value. The dialog box is displayed.

#. In the **Port Status** column of the associated server, check the port status.

   To enable the port again, click the **Edit Policy** to select server, and then bind the server. For details about how to edit a policy, see :ref:`Editing a Policy <hss_01_0604__section466884823118>`.

FAQs
----

**What can I do if the port fails to be enabled?**

-  Possible cause 1: The port is occupied by other services.

   Solution: Add other idle ports by editing the policy.

-  Possible cause 2: System resources are insufficient.

   Solution: Free up some system resources, click the **Edit Policy** to select server, and then bind the server. For details about how to edit a policy, see :ref:`Editing a Policy <hss_01_0604__section466884823118>`.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

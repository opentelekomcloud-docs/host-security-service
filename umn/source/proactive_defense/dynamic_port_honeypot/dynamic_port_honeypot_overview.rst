:original_name: hss_01_0599.html

.. _hss_01_0599:

Dynamic Port Honeypot Overview
==============================

What is Dynamic Port Honeypot?
------------------------------

The dynamic port honeypot function is a deception trap. It uses a real port as a bait port to induce attackers to access the network. In the horizontal penetration scenario, the function can effectively detect attackers' scanning, identify faulty servers, and protect real resources of the user.

You can enable the dynamic port honeypot using recommended ports or user-defined ports to deceive compromised servers and reduce the risk of resources intrusion. :ref:`Figure 1 <hss_01_0599__fig92949271246>` shows how the dynamic port honeypot works.

.. _hss_01_0599__fig92949271246:

.. figure:: /_static/images/en-us_image_0000001845167469.png
   :alt: **Figure 1** Dynamic port honeypot protection

   **Figure 1** Dynamic port honeypot protection

How Do I Use Dynamic Port Honeypot?
-----------------------------------

:ref:`Figure 2 <hss_01_0599__fig157883339143>` shows the process of using the dynamic port honeypot.

.. _hss_01_0599__fig157883339143:

.. figure:: /_static/images/en-us_image_0000001956208446.png
   :alt: **Figure 2** Process of using the dynamic port honeypot

   **Figure 2** Process of using the dynamic port honeypot

.. table:: **Table 1** Process of using the dynamic port honeypot

   +-------------------------------------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Operation                                                                     | Description                                                                                                                                                                                |
   +===============================================================================+============================================================================================================================================================================================+
   | :ref:`Creating a Protection Policy for a Dynamic Honeypot Port <hss_01_0600>` | Enable the server port of dynamic port function, configure the source IP address whitelist, and bind the protected server.                                                                 |
   +-------------------------------------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`Viewing and Handling Honeypot Protection Events <hss_01_0601>`          | The dynamic port honeypot function reports an alarm when a potentially compromised server proactively connects to a honeypot port. You can handle the alarm based on service requirements. |
   +-------------------------------------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Constraints and Limitations
---------------------------

-  Dynamic port honeypots apply only to servers that are not bound to EIPs.
-  Dynamic port honeypots are available only in HSS premium, web tamper protection, and container editions.
-  To use the dynamic port honeypots, ensure that the agent installed on the server falls within the following ranges. For more information, see :ref:`Upgrading the Agent <hss_01_0462>`.

   -  Linux: 3.2.10 or later.
   -  Windows: 4.0.22 or later.

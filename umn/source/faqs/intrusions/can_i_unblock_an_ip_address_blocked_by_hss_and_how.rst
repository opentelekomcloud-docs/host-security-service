:original_name: hss_01_0013.html

.. _hss_01_0013:

Can I Unblock an IP Address Blocked by HSS, and How?
====================================================

Whether you can unblock an IP address depends on why it was blocked. An IP address will be blocked if it is regarded as the source of a brute-force attack, listed in the common IP blacklist, or not in the IP whitelist you set.

Brute-force Attack IP Address
-----------------------------

-  If a brute force attack is detected, HSS blocks the attack source IP address for 12 hours by default. If a blocked IP address does not perform brute-force attacks in the default blocking duration, it will be automatically unblocked.

-  If you are sure that a source IP address can be trusted, you can manually unblock it. Choose **Detection** > **Alarms**, click **View Details** under **Blocked IP Addresses**, and unblock the IP address in the displayed slide-out panel.

   If you manually unblocked an IP address, but incorrect password attempts from this IP address exceed the threshold again, this IP address will be blocked again.

IP Address in the Common IP Blacklist
-------------------------------------

You cannot manually unblock such IP addresses.

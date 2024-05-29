:original_name: hss_01_0287.html

.. _hss_01_0287:

How Do I Unblock an IP Address?
===============================

HSS will block an IP address if it has five or more brute-force attack attempts detected within 30 seconds, or 15 or more brute-force attack attempts detected within 3600 seconds. If a normal IP address is blocked by mistake (for example, after O&M personnel enter incorrect passwords for multiple times), you can unblock the IP address.

If you manually unblocked an IP address, but incorrect password attempts from this IP address reach the threshold again, this IP address will be blocked again.

.. note::

   -  The default blocking duration is 12 hours.
   -  If a blocked IP address does not perform brute-force attacks in the default blocking duration, it will be automatically unblocked.

Procedure
---------

#. Log in to the management console.
#. In the navigation tree on the left, choose **Detection** > **Alarms** and click **Server Alarms**.
#. In the **Alarm Statistics** area, click **View Details** under **Blocked IP Addresses**.
#. In the blocked IP address list, select an IP address and click **Cancel Interception**.

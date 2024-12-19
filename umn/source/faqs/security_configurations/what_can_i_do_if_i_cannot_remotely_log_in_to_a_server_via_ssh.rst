:original_name: hss_01_0436.html

.. _hss_01_0436:

What Can I Do If I Cannot Remotely Log In to a Server via SSH?
==============================================================

Symptoms
--------

You can log in to a server via the console but not via SSH.

Possible Causes
---------------

-  A server will be blocked if it is regarded as a suspicious server performing brute-force attacks (for example, the number of incorrect password attempts reaches 5 within 30 seconds).

-  The SSH login IP whitelist is enabled. Your login IP addresses have not been added to the login whitelist.

   If you enable the SSH login IP address whitelist, SSH logins will be allowed only from whitelisted IP addresses.

Solution
--------

#. Check whether your login IP address was blocked because it was regarded as a source of brute-force attacks.

   -  If yes, perform the following steps:

      a. Log in to the console.
      b. In the navigation pane, choose **Intrusion Detection** > **Alarms**.
      c. Select the **Server Alarms** tab. Click the View Details in the **Blocked IP Addresses** area. The **Blocked IP Addresses** page is displayed.
      d. Select the target attack source IP address and click **Unblock** above the list to unblock the IP address.

   -  If your login IP address was not blocked for this reason, go to :ref:`2 <hss_01_0436__en-us_topic_0243005744_li13860915135115>`.

#. .. _hss_01_0436__en-us_topic_0243005744_li13860915135115:

   Check whether your login IP address is blocked because it is not whitelisted and the SSH login IP whitelist is enabled.

   -  If your login IP address was not blocked for this reason, add the IP address to the SSH login IP address whitelist.
   -  If your login IP address was not blocked for this reason, contact technical support.

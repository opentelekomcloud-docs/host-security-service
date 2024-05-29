:original_name: hss_01_0008.html

.. _hss_01_0008:

How Does HSS Intercept Brute Force Attacks?
===========================================

Types of Detectable Brute Force Attacks
---------------------------------------

HSS can detect the following types of brute force attacks:

-  Windows: SqlServer (automatic interception is not supported currently) and Rdp
-  Linux: MySQL, vfstp, and SSH

If MySQL or VSFTP is installed on your server, after HSS is enabled, the agent will add rules to iptables to prevent MySQL and VSFTP brute force attacks. When detecting a brute-force attack, HSS will add the source IP address to the blocking list. The added rules are highlighted below.


.. figure:: /_static/images/en-us_image_0000001568317649.png
   :alt: **Figure 1** Added rules

   **Figure 1** Added rules

.. important::

   Existing iptables rules are used for blocking brute-force attacks. You are advised to keep them. If they are deleted, HSS will not be able to protect MySQL or VSFTP from brute-force attacks.

How Brute Force Attacks Are Intercepted
---------------------------------------

Brute-force attacks are a type of common intrusion attacks. Attackers submit many server passwords until eventually guessing correctly and gaining control over a server.

HSS uses brute-force detection algorithms and an IP address blacklist to effectively prevent brute-force attacks and block attacking IP addresses. The blocking duration is 12 hours. If a blocked IP address does not perform brute-force attacks in the default blocking duration, it will be automatically unblocked.

.. note::

   If HSS detects account cracking attacks on servers using Kunpeng EulerOS (EulerOS with ARM), it does not block the source IP addresses and only generates alarms. The SSH login IP address whitelist does not take effect for such servers.

Alarm Policies
--------------

-  If a hacker successfully cracks the password and logs in to a server, a real-time alarm will be immediately sent to specified recipients.
-  If a brute-force attack and risks of account hacking are detected, a real-time alarm will be immediately sent to specified recipients.
-  If a brute-force attack is detected and failed, and no unsafe settings (such as weak passwords) are detected on the server, no real-time alarms will be sent. HSS will summarize all attacks in a day in its daily alarm report. You can also view blocked attacks on the **Detection** > **Alarms** page of the HSS console.

Viewing Brute Force Cracking Detection Results
----------------------------------------------

#. Log in to the management console.
#. In the navigation pane, choose **Detection** > **Alarms**.
#. View the brute force cracking detection result of the server or container.

   -  View the brute force cracking detection result of the server.

      a. Click the **Server Alarms** tab.
      b. In the **Alarm Types** area, select **Abnormal User Behavior** > **Brute-force attacks** to view alarm event records on the protected server.
      c. Click **View Details** in the **Blocked IP Addresses** area to view the blocked attack source IP address, attack type, blocking status, blocking times, blocking start time, and latest blocking time.

         -  **Blocked** indicates the brute-force attack has been blocked by HSS.
         -  **Canceled** indicates you have unblocked the source IP address of the brute force attack.

            .. note::

               The default blocking duration is 12 hours. If a blocked IP address does not perform brute-force attacks in the default blocking duration, it will be automatically unblocked.

   -  View the brute force cracking detection result of a container.

      a. Click the **Container Alarms** tab.
      b. In the **Alarm Types** area, select **Abnormal User Behavior** > **Brute-force attacks** to view alarm event records on the protected container.

Managing Blocked IP Addresses
-----------------------------

-  If a server is frequently attacked, you are advised to fix its vulnerabilities in a timely manner and eliminate risks.
-  If a valid IP address is blocked by mistake (for example, after O&M personnel enter incorrect passwords for multiple times), :ref:`manually unblock the IP address <hss_01_0287>`.

   .. important::

      If you manually unblocked an IP address, but incorrect password attempts from this IP address exceed the threshold again, this IP address will be blocked again.

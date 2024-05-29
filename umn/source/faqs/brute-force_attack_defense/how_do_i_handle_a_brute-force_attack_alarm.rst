:original_name: hss_01_0183.html

.. _hss_01_0183:

How Do I Handle a Brute-force Attack Alarm?
===========================================

-  If a brute-force attack succeeded, take immediate measures to prevent attackers from further actions, such as breaching data, performing DDoS attacks, or implanting ransomware, miners, or Trojans.
-  If a brute-force attack was blocked, take immediate measures to enhance your servers.

Mind map for troubleshooting
----------------------------

The following mind map describes how to handle a brute-force attack alarm.


.. figure:: /_static/images/en-us_image_0000001568317709.png
   :alt: **Figure 1** Mind map for troubleshooting

   **Figure 1** Mind map for troubleshooting

Handling the Alarm of a Successful Brute-force Attack
-----------------------------------------------------

If you received an alarm notification indicating that your account had been cracked, you are advised to harden your servers as soon as possible.

#. Log in to the management console.

#. Check whether the IP address that triggered the alarm is valid.

   a. In the navigation pane, choose **Detection** > **Alarms**.
   b. In the **Alarm Types** area, select **Abnormal User Behavior** > **Abnormal logins** to view abnormal login alarm events.
   c. Click the alarm event name. On the details page that is displayed, check the login IP address.

      -  If the IP address is from a normal user (for example, who entered incorrect password for multiple times but logged in before their account is blocked), your server is not intruded. In this case, you can click **Handle** and ignore the event.

      -  If the IP address is invalid, your server may have been intruded.

         In this case, mark this event as handled, log in to the intruded server, and change its password to a stronger one. For details, see :ref:`How Do I Set a Secure Password? <hss_01_0166>`

#. Check for and eliminate malicious programs.

   a. In the navigation pane, choose **Detection** > **Alarms**.

   b. In the **Alarm Types** area, select **Malware** > **Unclassified malware** to filter the unclassified malware.

   c. In the **Alarm Type** column, select **Malicious program** and check alarm events.

      You can click an alarm name to view alarm event details.

      -  If you find malicious programs implanted in your servers, locate them based on their process paths, users running them, and startup time.

         To kill a malicious program in an alarm event, click **Handle** in the **Operation** column of an alarm and select **Isolate and kill**.

      -  If you have confirmed that all the malicious program alarms are false, go to :ref:`Step 8 <hss_01_0183__li206265374135>`.

#. .. _hss_01_0183__li206265374135:

   Check for suspicious account change records.

   a. In the navigation pane on the left, choose **Asset Management** > **Server Fingerprints**.
   b. Click the **Account Information** tab. Detect suspicious account change records to prevent attackers from creating accounts or escalating account permissions (for example, adding login permissions to an account)..

#. **Check and handle invalid accounts.**

   a. In the navigation pane, choose **Detection** > **Alarms**.
   b. In the **Alarm Types** area, select **Abnormal User Behavior** > **Invalid accounts**. View and handle the invalid account alarms.

#. Check for and fix unsafe settings.

   Check for and fix weak password complexity policies and unsafe software settings on your servers.

Handling the Alarm of a Blocked Brute-force Attack
--------------------------------------------------

If you have enabled , HSS will protect your servers against brute-force attacks.

You can configure a login security policy to specify the brute force cracking determination mode and blocking duration.

If you have not configured any login security detection policy, the following default login security policy is used: HSS will block an IP address if it has five or more brute-force attack attempts detected within 30 seconds, or 15 or more brute-force attack attempts detected within 3,600 seconds.

If you receive an alarm indicating that an attack source IP address is blocked, check whether the source IP address is a trusted IP address.

**Constraints and Limitations**

-  Linux

   On servers running the EulerOS with ARM, HSS does not block the IP addresses suspected of SSH brute-force attacks, but only generates alarms.

-  Windows

   -  Authorize the Windows firewall when you enable protection for a Windows server. Do not disable the Windows firewall during the HSS in-service period. If the Windows firewall is disabled, HSS cannot block brute-force attack IP addresses.
   -  If the Windows firewall is manually enabled, HSS may also fail to block brute-force attack IP addresses.

**Procedure**

#. Log in to the management console.

#. Choose **Detection** > **Alarms**. Choose **Abnormal User Behavior** > **Brute-force attacks** to view account brute force events.

   Brute-force attack alarms will be generated if:

   -  The system uses weak passwords, is under brute-force attacks, and attacker IP addresses are blocked.
   -  Users fail to log in after several incorrect password attempts, and their IP addresses are blocked.

#. Check whether the login IP address triggering the alarm is valid.

   -  If the IP address is valid,

      -  To handle a false alarm, click **Handle** in the row of the alarm event. Mark this event as **Ignore** or **Add to Login Whitelist**.

         This does not unblock the IP address.

      -  To unblock the IP address, click **View Details** under **Blocked IP Addresses**, select the IP address, and unblock it. Alternatively, you can just wait for it to be automatically unblocked when its blocking duration expires. The default blocking duration is 12 hours.

   -  If the source IP address is invalid or unknown,

      Mark this event as handled.

      Immediately log in to your server and change your password to a stronger one.

Helpful Links
-------------

-  :ref:`How Does HSS Intercept Brute Force Attacks? <hss_01_0008>`
-  :ref:`How Do I Unblock an IP Address? <hss_01_0287>`

:original_name: hss_01_0026.html

.. _hss_01_0026:

Viewing Server Alarms
=====================

HSS displays alarm and event statistics and their summary all on one page. You can have a quick overview of alarms, including the numbers of urgent alarms, total alarms, servers with alarms, blocked IP addresses, and isolated files.

The **Events** page displays the alarm events generated in the last 30 days. You can manually handle the alarmed items.

The status of a handled event changes from **Unhandled** to **Handled**.

Constraints and Limitations
---------------------------

-  To skip the checks on high-risk command execution, privilege escalations, reverse shells, abnormal shells, or web shells, manually disable the corresponding policies in the policy groups on the **Policies** page. HSS will not check the servers associated with disabled policies.
-  Other detection items cannot be manually disabled.
-  Servers that are not protected by HSS do not support operations related to alarms and events.


Viewing Server Alarms
---------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane on the left, choose **Intrusion Detection** > **Alarms** and click **Server Alarms**.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.


   .. figure:: /_static/images/en-us_image_0000001621827002.png
      :alt: **Figure 1** Server alarms

      **Figure 1** Server alarms

   -  **Viewing the container alarms of a certain type**

      In the **Event Types** area, select an alarm event type to view the corresponding alarm event list. In the alarm list, you can view the alarm name, alarm threat level, and affected servers.

   -  **Viewing the alarms of a certain type or ATT&CK phase**

      In the **Alarms to Be Handled** area, you can select an alarm type and an ATT&CK phase to view the alarms of the selected type. For details, see :ref:`ATT&CK attack phase description <hss_01_0026__table6516818161215>`.

      .. note::

         Adversarial Tactics, Techniques and Common Knowledge (ATT&CK) is a framework that helps organizations understand the cyber adversary tactics and techniques used by threat actors across the entire attack lifecycle.

      .. _hss_01_0026__table6516818161215:

      .. table:: **Table 1** ATT&CK phases

         +----------------------+-------------------------------------------------------------------------+
         | ATT&CK Phase         | Description                                                             |
         +======================+=========================================================================+
         | Reconnaissance       | Attackers seek vulnerabilities in your system or network.               |
         +----------------------+-------------------------------------------------------------------------+
         | Initial Access       | Attacker try to enter your system or network.                           |
         +----------------------+-------------------------------------------------------------------------+
         | Execution            | Attackers try to run malicious code.                                    |
         +----------------------+-------------------------------------------------------------------------+
         | Persistence          | Attackers try to maintain their foothold.                               |
         +----------------------+-------------------------------------------------------------------------+
         | Privilege Escalation | Attackers try to obtain higher permissions.                             |
         +----------------------+-------------------------------------------------------------------------+
         | Defense Evasion      | Attackers try to avoid being detected.                                  |
         +----------------------+-------------------------------------------------------------------------+
         | Credential Access    | Attackers try to steal account names and passwords.                     |
         +----------------------+-------------------------------------------------------------------------+
         | Command and Control  | Attackers try to communicate with compromised machines to control them. |
         +----------------------+-------------------------------------------------------------------------+
         | Impact               | Attackers try to manipulate, interrupt, or destroy your system or data. |
         +----------------------+-------------------------------------------------------------------------+

   -  **Viewing the details of a server alarm**

      You can click the alarm name of an event to view the alarm details.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

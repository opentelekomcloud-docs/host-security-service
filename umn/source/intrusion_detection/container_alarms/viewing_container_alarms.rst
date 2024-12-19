:original_name: hss_01_0313.html

.. _hss_01_0313:

Viewing Container Alarms
========================

HSS displays alarm and event statistics and their summary all on one page. You can have a quick overview of alarms, including the numbers of containers with alarms, handled alarms, and unhandled alarms.

The **Events** page displays the alarm events generated in the last 30 days.

The status of a handled event changes from **Unhandled** to **Handled**.

Constraints
-----------

Servers that are not protected by HSS do not support operations related to alarms and events.


Viewing Container Alarms
------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane, choose **Intrusion Detection** > **Alarms** and click the **Container Alarms** tab to view container alarms and events.


   .. figure:: /_static/images/en-us_image_0000001670234665.png
      :alt: **Figure 1** Container alarms

      **Figure 1** Container alarms

   .. table:: **Table 1** Container alarm statistics

      +------------------------+---------------------------------------------------------------------------------------------------------------------+
      | Parameter              | Description                                                                                                         |
      +========================+=====================================================================================================================+
      | Urgent Alarms          | Number of alarms that need to be handled immediately. You can click a value to view the corresponding alarm events. |
      +------------------------+---------------------------------------------------------------------------------------------------------------------+
      | Total Alarms           | Total number of alarms reported on your assets. You can click the number to view all alarms.                        |
      +------------------------+---------------------------------------------------------------------------------------------------------------------+
      | Containers with Alarms | Number of containers for which alarms are generated.                                                                |
      +------------------------+---------------------------------------------------------------------------------------------------------------------+
      | Handled Alarms         | Number of handled alarms                                                                                            |
      +------------------------+---------------------------------------------------------------------------------------------------------------------+

   -  **Viewing the container alarms of a certain type**

      In the **Event Types** area, select an alarm event type to view the corresponding alarm event list. In the alarm event list, you can view the alarm threat level, alarm name, and affected container name.

   -  **Viewing the alarms of a certain type or ATT&CK phase**

      In the **Alarms to Be Handled** area, select an alarm type or att&ck phase. For details, see :ref:`ATT&CK attack phase description <hss_01_0313__table6516818161215>`.

      .. note::

         Adversarial Tactics, Techniques and Common Knowledge (ATT&CK) is a framework that helps organizations understand the cyber adversary tactics and techniques used by threat actors across the entire attack lifecycle.

      .. _hss_01_0313__table6516818161215:

      .. table:: **Table 2** ATT&CK phases

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

   -  **Viewing details about container alarms and events**

      Click an alarm name to go to its details page. You can view the container ID, IP address, VM name, and image ID.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

:original_name: hss_01_0546.html

.. _hss_01_0546:

Risk Statistics
===============

On the dashboard page of the HSS console, you can learn the security status and risks of all your servers and containers in real time, including the risk index, risk trend, top 5 event types, and service quota.

.. note::

   If you have enabled the enterprise project function, you can select your enterprise project from the **Enterprise project** drop-down list to check server risk overview of the project. If you select **All projects**, the risk overview of servers in all the projects in this region is displayed.

#. Log in to the management console.
#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.
#. In the navigation pane, choose **Dashboard**.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.

Asset Risk Index (Last 24 Hours)
--------------------------------


.. figure:: /_static/images/en-us_image_0000001782400597.png
   :alt: **Figure 1** Asset risk index (last 24 hours)

   **Figure 1** Asset risk index (last 24 hours)

You can check the risks in protected servers and containers in the last 24 Hours.

To handle the risks, click **Handle Now**. The **Risks** pane will be displayed on the right. You can handle risks by referring to the corresponding guidance. You can handle the following types of risks:

-  Intrusions
-  Vulnerabilities
-  Unsafe Settings

To check your asset security, click **Scan**.

Protection Status (Last 24 Hours)
---------------------------------


.. figure:: /_static/images/en-us_image_0000001614183089.png
   :alt: **Figure 2** Protection Status

   **Figure 2** Protection Status

You can check the numbers of protected and unprotected servers and nodes.

To enable protection for a server, click **Enable Protection**.

Risks (Latest 24 Hours)
-----------------------


.. figure:: /_static/images/en-us_image_0000001614383481.png
   :alt: **Figure 3** Risks

   **Figure 3** Risks

You can check the number of server asset risks, server vulnerabilities, server baselines, and container risks, and their comparison with the previous day.


Risk Statistics
---------------


.. figure:: /_static/images/en-us_image_0000001564103542.png
   :alt: **Figure 4** Risk trend

   **Figure 4** Risk trend

You can check the risk trend in the last 24 hours, last 3 days, last 7 days, and last 30 days.

.. table:: **Table 1** Risk statistics

   +-----------------------------------+-------------------------------------+
   | Category                          | Event                               |
   +===================================+=====================================+
   | Asset risks                       | -  Accounts                         |
   |                                   | -  Open ports                       |
   |                                   | -  Processes                        |
   |                                   | -  Installed software               |
   |                                   | -  Auto-started items               |
   |                                   | -  Web applications                 |
   |                                   | -  Web services                     |
   |                                   | -  Web frameworks                   |
   |                                   | -  Websites                         |
   |                                   | -  Middleware                       |
   |                                   | -  Databases                        |
   |                                   | -  Kernel modules                   |
   +-----------------------------------+-------------------------------------+
   | Server vulnerabilities            | -  Linux vulnerabilities            |
   |                                   | -  Windows vulnerabilities          |
   |                                   | -  Web-CMS vulnerabilities          |
   |                                   | -  Application vulnerabilities      |
   +-----------------------------------+-------------------------------------+
   | Server baseline risks             | -  Password complexity policy check |
   |                                   | -  Common weak password check       |
   |                                   | -  Unsafe configuration check       |
   +-----------------------------------+-------------------------------------+
   | Container risks                   | -  Local image vulnerabilities      |
   |                                   | -  Private image vulnerabilities    |
   |                                   | -  Malicious files in images        |
   |                                   | -  Image baseline                   |
   +-----------------------------------+-------------------------------------+

Intrusions (Last 24 Hours)
--------------------------


.. figure:: /_static/images/en-us_image_0000001614384633.png
   :alt: **Figure 5** Intrusions (last 24 hours)

   **Figure 5** Intrusions (last 24 hours)

You can check the total number of intrusions detected on servers and containers, and the severities of the intrusions.

These intrusion statistics are updated at 00:00 every day.

Top 5 Events
------------


.. figure:: /_static/images/en-us_image_0000001564104674.png
   :alt: **Figure 6** Top 5 events

   **Figure 6** Top 5 events

For servers protected by the enterprise, premium, or container security edition, you can check the top five types of intrusion events detected in the last 24 hours, last 3 days, last 7 days, or last 30 days; and the number of each type of events.

If no data is displayed due to connection problems, fix your network and click |image2| to retrieve data again.

Real-time Alarms
----------------

You can check real-time alarms.

Check the latest five unhandled intrusion events in the last 24 hours, including their severities, alarm names, occurrence time, and statuses.

-  To check alarm details, click an alarm name.
-  To handle an alarm, click **Handle** in its **Operation** column. After the alarm is handled, it will be removed from the list. The list refreshes and displays the latest five intrusion events that have not been handled in the last 24 hours.
-  To check more alarm events, click **View More**.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png
.. |image2| image:: /_static/images/en-us_image_0000001568637417.png

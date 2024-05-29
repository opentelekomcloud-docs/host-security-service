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

Procedure
---------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

#. In the navigation pane, choose **Detection** > **Alarms** and click the **Container Alarms** tab to view container alarms and events.


   .. figure:: /_static/images/en-us_image_0000001670234665.png
      :alt: **Figure 1** Viewing container alarms

      **Figure 1** Viewing container alarms

   -  View the overview of container alarms and events.

      -  **Alarm Statistics**: You can view the number of containers that have alarms and the number of alarms to be handled and that have been handled.
      -  **Threats**: You can view the number of alarms in a container by severity.
      -  **Top 5 Events**: You can view the top 5 events with the largest number of alarms in a container.

   -  View the container alarms of a certain type.

      In the **Event Types** area, select an alarm event type to view the corresponding alarm event list. In the alarm event list, you can view the alarm threat level, alarm name, and affected container name.

   -  View details about container alarms and events.

      Click an alarm name to go to its details page. You can view the container ID, IP address, VM name, and image ID.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

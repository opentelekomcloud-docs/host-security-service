:original_name: hss_01_0414.html

.. _hss_01_0414:

Handling Container Alarms
=========================

HSS displays alarm and event statistics and their summary all on one page. You can have a quick overview of alarms, including the numbers of containers with alarms, handled alarms, and unhandled alarms.

The **Events** page displays the alarms generated in the last 30 days.

The status of a handled alarm changes from **Unhandled** to **Handled**.

Constraints
-----------

Servers that are not protected by HSS do not support operations related to alarms and events.

Procedure
---------

This section describes how you should handle alarms to enhance server security.

.. note::

   Do not fully rely on alarm handling to defend against attacks, because not every issue can be detected in a timely manner. You are advised to take more measures to prevent threats, such as checking for and fixing vulnerabilities and unsafe settings.

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

#. In the navigation pane on the left, choose **Detection** > **Alarms**, and click **Container Alarms**.


   .. figure:: /_static/images/en-us_image_0000001670554661.png
      :alt: **Figure 1** Viewing container alarms

      **Figure 1** Viewing container alarms

   .. table:: **Table 1** Alarm statistics

      +-----------------------------------+------------------------------------------------------------------------+
      | Alarm Event                       | Description                                                            |
      +===================================+========================================================================+
      | Containers with Alarms            | Number of containers for which alarms are generated.                   |
      +-----------------------------------+------------------------------------------------------------------------+
      | Alarms to be Handled              | Number of alarms to be handled.                                        |
      |                                   |                                                                        |
      |                                   | By default, all unhandled alarms are displayed on the **Events** page. |
      +-----------------------------------+------------------------------------------------------------------------+
      | Handled Alarms                    | Number of handled alarms.                                              |
      +-----------------------------------+------------------------------------------------------------------------+

#. Handle alarms.

   .. note::

      Alarms are displayed on the **Container Alarms** page. Here you can check up to 30 days of historical alarms.

      Check and handle alarms as needed. The status of a handled alarm changes from **Unhandled** to **Handled**. HSS will no longer collect its statistics.

   -  Handling selected alarms in batches

      a. Select an event type, select multiple alarms, and click **Batch Handle**.
      b. In the dialog box that is displayed, select a handling method, confirm the information, and click **OK**. For more information, see :ref:`Table 2 <hss_01_0414__table58569395296>`.

   -  Handling a single alarm

      a. Select an event type, and click **Handle** in the **Operation** column of an alarm.
      b. In the dialog box that is displayed, select a handling method, confirm the information, and click **OK**. For more information, see :ref:`Table 2 <hss_01_0414__table58569395296>`.

   .. _hss_01_0414__table58569395296:

   .. table:: **Table 2** Handling alarm events

      +-----------------+------------------------------------------------------------------------------------------+
      | Action          | Description                                                                              |
      +=================+==========================================================================================+
      | Ignore          | Ignore the current alarm. Any new alarms of the same type will still be reported by HSS. |
      +-----------------+------------------------------------------------------------------------------------------+
      | Mark as handled | Mark the event as handled. You can add remarks for the event to record more details.     |
      +-----------------+------------------------------------------------------------------------------------------+

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

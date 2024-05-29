:original_name: hss_01_0028.html

.. _hss_01_0028:

Managing the Alarm Whitelist
============================

You can configure the alarm whitelist to reduce false alarms. Events can be deleted from the whitelist.

Whitelisted events will not trigger alarms.

On the **Alarms** page, you can add falsely reported alarms to the alarm whitelist. After an alarm is added to the whitelist, HSS will not generate alarms or collect statistics on it.

Adding Events to the Alarm Whitelist
------------------------------------

.. table:: **Table 1** Configuring the alarm whitelist

   +-----------------------------------+--------------------------------------------------------------------+
   | Method                            | Description                                                        |
   +===================================+====================================================================+
   | Add to alarm whitelist            | Choose to add the alarm to the whitelist when handling it.         |
   |                                   |                                                                    |
   |                                   | The following types of events can be added to the alarm whitelist: |
   |                                   |                                                                    |
   |                                   | -  Reverse shells                                                  |
   |                                   | -  Ransomware                                                      |
   |                                   | -  Malicious programs                                              |
   |                                   | -  Web shell                                                       |
   |                                   | -  Abnormal process behaviors                                      |
   |                                   | -  Process privilege escalations                                   |
   |                                   | -  File privilege escalations                                      |
   |                                   | -  High-risk command executions                                    |
   |                                   | -  Malicious programs                                              |
   |                                   | -  Important file changes                                          |
   |                                   | -  File/Directory changes                                          |
   |                                   | -  Abnormal shells                                                 |
   |                                   | -  Suspicious crontab tasks                                        |
   |                                   | -  Invalid accounts                                                |
   |                                   | -  Common vulnerability exploits                                   |
   +-----------------------------------+--------------------------------------------------------------------+

Checking the Alarm Whitelist
----------------------------

Perform the following steps to check the alarm whitelist:

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

#. In the navigation pane on the left, choose **Detection** > **Whitelists**.

#. Click **Alarm Whitelist** to view the added alarm whitelist. For more information, see :ref:`Table 2 <hss_01_0028__table1213284433320>`.

   .. _hss_01_0028__table1213284433320:

   .. table:: **Table 2** Parameter description

      ================== =============================================
      Parameter Name     Description
      ================== =============================================
      Alarm Type         Name of the alarm whitelist type.
      SHA256             Hash value of the target file.
      Description        Description of the target whitelist.
      Added              Time when an alarm is added to the whitelist.
      Enterprise Project Enterprise project
      ================== =============================================

Related Operations
------------------

**Removing alarms from the whitelist**

To remove an alarm from the whitelist, select it and click **Delete**.

.. note::

   -  Exercise caution when performing this operation. Whitelisted alarms cannot be restored after removal, and will be reported once triggered.
   -  After an alarm is deleted from the whitelist, the handling status of the events associated with the alarm is not updated. To change the status, choose **Detection** > **Alarms**, click **Handle** in the **Operation** column of an event, and select **Remove from whitelist**.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

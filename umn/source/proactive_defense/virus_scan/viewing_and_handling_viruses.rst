:original_name: hss_01_0585.html

.. _hss_01_0585:

Viewing and Handling Viruses
============================

After the virus scanning is complete, the system handles the infected files based on the handling policy selected. The handling policies are as follows:

-  **Automatic Handling**: Virus files that have been further confirmed are automatically isolated. Suspicious files are labeled with suspicious and need to be handled after manual confirmation.
-  **Manual Handling**: Alarms are generated only for detected infected files. You need to manually confirm the files before handling them.

Prerequisites
-------------

A virus scanning task has been executed. For details, see :ref:`Scanning for Viruses <hss_01_0584>`.


Viewing and Handling Viruses
----------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. Choose **Prevention** > **Virus Scan**.

#. View the scanned virus files.

#. In the **Operation** column of a virus file, click **Handle**.

   You can also select multiple virus files and click **Batch Handle** above the list to handle them in batches.

#. In the **Handle Infected Files** dialog box, select a virus-infected file handling method. For details about the processing modes, see :ref:`Virus-infected file handling methods <hss_01_0585__table1186017570241>`.

   .. _hss_01_0585__table1186017570241:

   .. table:: **Table 1** Virus-infected file handling methods

      +------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter              | Description                                                                                                                                                                   |
      +========================+===============================================================================================================================================================================+
      | Mark as handled        | You can manually handle the virus-infected file on the server.                                                                                                                |
      +------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Ignore                 | Ignore the virus-infected file alarm. If the virus-infected file alarm event occurs again, HSS generates an alarm.                                                            |
      +------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Add to alarm whitelist | If you confirm that the virus file is falsely reported, you can add it to the alarm whitelist. After a file is added to whitelist, HSS will not generate alarms for the file. |
      +------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Isolating files        | After a file is isolated, the read/write operation cannot be performed on the virus-infected file.                                                                            |
      +------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Click **OK**.

   After the alarm is handled, the status of the virus file alarm event changes to **Handled**.

Exporting Virus-infected File Alarms
------------------------------------

#. Log in to the management console.
#. Click |image2| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.
#. Choose **Prevention** > **Virus Scan**.
#. Above the virus-infected file alarm event list, click **Export** to export all virus-infected file alarm events to the local PC.
#. View the export status in the upper part of the virus scan page. After the export is successful, obtain the exported information from the default file download address on the local host.

   .. important::

      Do not close the browser page during the export. Otherwise, the export task will be interrupted.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png
.. |image2| image:: /_static/images/en-us_image_0000001517477398.png

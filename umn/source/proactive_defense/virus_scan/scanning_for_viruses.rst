:original_name: hss_01_0584.html

.. _hss_01_0584:

Scanning for Viruses
====================

Once a static virus file is started, it may become a malicious process and become a security risk of servers. Therefore, scanning static virus files is important in server security protection. HSS virus scan function can scan virus files on servers and provides the following virus scan methods:

-  **Quick Scan**: Quick virus scanning tasks can save time and costs. This function scans and removes preset key system files and directories.
-  **Full-disk Scan**: A time-consuming full-disk virus scanning can be implemented on servers.
-  **Custom Scan**: You can customize virus scanning tasks as required.

Constraints
-----------

-  A virus scan uses a lot of memory, CPU, and I/O resources. Perform this operation during off-peak hours.
-  A full-disk scan does not check network directories.

Quick Scan
----------

#. Log in to the management console.
#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.
#. Choose **Prevention** > **Virus Scan**.
#. Click **Quick Scan**. The dialog box is displayed.
#. Set parameters related to the quick scan task as prompted.

   -  **Task Name**: You can customize a task name.
   -  **Select Server**: Select the server for which you want to perform quick scan.

      .. note::

         A server being scanned cannot be selected for another scan task.

   -  **Handling Policy**: Select the handling mode for the detected virus files.

      -  **Automatic Handling**: Virus files that have been further confirmed are automatically isolated. Suspicious files are labeled with suspicious and need to be handled after manual confirmation.
      -  **Manual Handling**: Alarms are generated only for detected infected files. You need to manually confirm the files before handling them.

#. Click **Scan** and start the scan task.

Full-disk Scan
--------------

#. Log in to the management console.
#. Click |image2| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.
#. Choose **Prevention** > **Virus Scan**.
#. Click **Full-disk Scan**. The dialog box is displayed.
#. Set parameters related to the full-disk scan task as prompted.

   -  **Task Name**: You can customize a task name.
   -  **Select Server**: Select the server for which you want to perform full-disk scan.

      .. note::

         A server being scanned cannot be selected for another scan task.

   -  **Handling Policy**: Select the handling mode for the detected virus files.

      -  **Automatic Handling**: Virus files that have been further confirmed are automatically isolated. Suspicious files are labeled with suspicious and need to be handled after manual confirmation.
      -  **Manual Handling**: Alarms are generated only for detected infected files. You need to manually confirm the files before handling them.

#. Click **Scan** and start the scan task.

Custom Scan
-----------

#. Log in to the management console.

#. Click |image3| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. Choose **Prevention** > **Virus Scan**.

#. Click **Custom Scan**.

#. Set the parameters of the **Custom Scan** policy as prompted. For details about the parameters, see :ref:`Custom antivirus policy parameters <hss_01_0584__table196361988474>`.

   .. _hss_01_0584__table196361988474:

   .. table:: **Table 1** Custom antivirus policy parameters

      +------------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                                | Description                                                                                                                                                                                        |
      +==========================================+====================================================================================================================================================================================================+
      | Task Name                                | Name of a custom antivirus task.                                                                                                                                                                   |
      +------------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | File Type                                | Type of the file to be scanned. Currently, the following types of files can be scanned:                                                                                                            |
      |                                          |                                                                                                                                                                                                    |
      |                                          | -  **Executable**: executable files and dynamic link libraries (DLLs), such as .exe, .dll, and .so files.                                                                                          |
      |                                          | -  **Compressed**: such as .zip, .rar, and .tar                                                                                                                                                    |
      |                                          | -  **Script**: such as .bat, .py, and .ps1                                                                                                                                                         |
      |                                          | -  **Document**: such as TXT, DOC, and PDF                                                                                                                                                         |
      |                                          | -  **Image**: such as BMP, JPG, and GIF                                                                                                                                                            |
      |                                          | -  **Audio & Video**: such as MP3, MP4, and FLV files                                                                                                                                              |
      +------------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | (Optional) Directory Settings            | Directory where virus-infected files need to be scanned. If this parameter is not set, full scan is performed by default. Full scan does not cover network directories.                            |
      +------------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | (Optional) Exclude Specified Directories | Directories that do not require virus scan.                                                                                                                                                        |
      +------------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Select Server                            | Servers to be scanned. Servers using any of the following policies cannot be selected:                                                                                                             |
      |                                          |                                                                                                                                                                                                    |
      |                                          | -  Policy whose **Startup Type** is **Scan Now**: A scan is in progress.                                                                                                                           |
      |                                          | -  Policy whose **Startup Type** is **Scan Later**: A custom scan policy using the same startup time as the current policy is in effect.                                                           |
      |                                          | -  Policy whose **Startup Type** is **Periodic Start**: A custom periodic scan has been scheduled.                                                                                                 |
      +------------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Handling Policy                          | Select the processing mode for the detected virus files.                                                                                                                                           |
      |                                          |                                                                                                                                                                                                    |
      |                                          | -  **Automatic Handling**: Virus files that have been further confirmed are automatically isolated. Suspicious files are labeled with suspicious and need to be handled after manual confirmation. |
      |                                          | -  **Manual Handling**: Alarms are generated only for detected infected files. You need to manually confirm the files before handling them.                                                        |
      +------------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Click **Scan** and start the scanning task.

Follow-up Procedure
-------------------

-  View the execution status of a scan job

   #. On the **Virus Scan** page, click the **Scan tasks** to view the execution status of virus scan tasks.

      To stop an ongoing scan task, click **Cancel** in the **Operation** column of the target scan task.

   #. Click |image4| to view the scan status and number of scanned files of each server.

      Click **Cancel** in the **Operation** column of the target server to stop scanning the server.

-  View and handle viruses

   After a virus scan task is complete, you can manually handle the detected virus files based on service requirements. For details, see :ref:`Viewing and Handling Viruses <hss_01_0585>`.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png
.. |image2| image:: /_static/images/en-us_image_0000001517477398.png
.. |image3| image:: /_static/images/en-us_image_0000001517477398.png
.. |image4| image:: /_static/images/en-us_image_0000001798279182.png

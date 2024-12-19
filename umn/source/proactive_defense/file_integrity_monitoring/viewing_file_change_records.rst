:original_name: hss_01_0361.html

.. _hss_01_0361:

Viewing File Change Records
===========================

File integrity monitoring provides change statistics, change types, and file change records, helping you learn about file changes in real time and detect malicious changes in a timely manner.

Viewing File Change Overview
----------------------------

#. Log in to the management console.
#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.
#. Choose **Prevention** > **File Integrity Monitoring**. Check the file change overview.

Viewing the File Change Records of a Single Server
--------------------------------------------------

#. In the server list, you can view the number of files and registry changes on a servers and the time when they were last changed.

#. Click a server name to go to the server change details page. You can view the file change details of the server.

   .. _hss_01_0361__table979905102414:

   .. table:: **Table 1** Server file change parameters

      +-----------------------+-----------------------------------------------------------------------+----------------------------------------------------------------+
      | Parameter             | Description                                                           | Example Value                                                  |
      +=======================+=======================================================================+================================================================+
      | File Name             | Name of a modified file.                                              | du                                                             |
      +-----------------------+-----------------------------------------------------------------------+----------------------------------------------------------------+
      | Path                  | Path of a modified file.                                              | ``-``                                                          |
      +-----------------------+-----------------------------------------------------------------------+----------------------------------------------------------------+
      | Change Description    | Description of the change.                                            | **SHA2560ba0c4b5e48e55a6** is changed to **4f6079f5b37d1513**. |
      |                       |                                                                       |                                                                |
      |                       | To view the change details, hover the cursor over the change content. |                                                                |
      +-----------------------+-----------------------------------------------------------------------+----------------------------------------------------------------+
      | Type                  | Type of a modified file. Its value can be:                            | File                                                           |
      |                       |                                                                       |                                                                |
      |                       | -  **File**                                                           |                                                                |
      |                       | -  **Registry**                                                       |                                                                |
      +-----------------------+-----------------------------------------------------------------------+----------------------------------------------------------------+
      | Action                | How a file was modified.                                              | Modify                                                         |
      |                       |                                                                       |                                                                |
      |                       | -  Create                                                             |                                                                |
      |                       | -  Modify                                                             |                                                                |
      |                       | -  Delete                                                             |                                                                |
      +-----------------------+-----------------------------------------------------------------------+----------------------------------------------------------------+
      | Last Modified         | The last time when a file was modified.                               | ``-``                                                          |
      +-----------------------+-----------------------------------------------------------------------+----------------------------------------------------------------+

Viewing the File Change Records of All Servers
----------------------------------------------

In the modified file list, you can view all file change records. For details, see :ref:`Table 1 <hss_01_0361__table979905102414>`.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

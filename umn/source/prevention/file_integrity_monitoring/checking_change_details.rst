:original_name: hss_01_0361.html

.. _hss_01_0361:

Checking Change Details
=======================

Constraints
-----------

Only premium, WTP, and container editions support file integrity-related operations.

Procedure
---------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

#. Choose **Prevention** > **File Integrity Monitoring**. The **Server** tab will be displayed.

#. Click the server name to go to the server change details page.

   .. _hss_01_0361__table979905102414:

   .. table:: **Table 1** Parameters about file changes

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
      +-----------------------+-----------------------------------------------------------------------+----------------------------------------------------------------+
      | Action                | How a file was modified.                                              | Modify                                                         |
      |                       |                                                                       |                                                                |
      |                       | -  Create                                                             |                                                                |
      |                       | -  Modify                                                             |                                                                |
      |                       | -  Delete                                                             |                                                                |
      +-----------------------+-----------------------------------------------------------------------+----------------------------------------------------------------+
      | Last Modified         | The last time when a file was modified.                               | ``-``                                                          |
      +-----------------------+-----------------------------------------------------------------------+----------------------------------------------------------------+

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

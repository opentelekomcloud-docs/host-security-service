:original_name: hss_01_0299.html

.. _hss_01_0299:

Managing SWR Private Images
===========================

Images in the private image repository come from SWR images. You can manually scan for and check reports on vulnerabilities, malicious files, software information, file information, baseline check, sensitive information.

Constraints
-----------

-  Only the HSS container edition supports this function.

-  Security scans can be performed only on Linux images.

Viewing Private Images
----------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

#. In the navigation pane, choose **Asset Management** **Container & Quota**. On the displayed page, click the **Container Images** tab and click **SWR private image**.


   .. figure:: /_static/images/en-us_image_0000001852172057.png
      :alt: **Figure 1** Accessing the private image list

      **Figure 1** Accessing the private image list

#. You can click **Update Private Images from SWR** to update self-owned images from SWR.

Scanning a Private Image
------------------------

You can choose all images, multiple images, or a single image and manually start a scan. The duration of a security scan depends on the scanned image size. Generally, scanning an image takes shorter than 3 minutes. After the scan is complete, click **View Report** to check the report.

Scan items of private images in SWR are as follows:

+-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Scan Item                         | Description                                                                                                                                                                                                      |
+===================================+==================================================================================================================================================================================================================+
| Vulnerability                     | Detect system and application vulnerabilities in images.                                                                                                                                                         |
+-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Malicious file                    | Detects malicious files in images.                                                                                                                                                                               |
+-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Software information              | Collects software information in an image.                                                                                                                                                                       |
+-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| File information                  | Collects file information in an image.                                                                                                                                                                           |
+-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Unsafe setting                    | -  Configuration check:                                                                                                                                                                                          |
|                                   |                                                                                                                                                                                                                  |
|                                   |    -  Checks the images configurations of CentOS 7, Debian 10, EulerOS, and Ubuntu16.                                                                                                                            |
|                                   |    -  Checks SSH configurations.                                                                                                                                                                                 |
|                                   |                                                                                                                                                                                                                  |
|                                   | -  Weak password check: detects weak passwords in images.                                                                                                                                                        |
|                                   | -  Password complexity check: detects insecure password complexity policies in images.                                                                                                                           |
+-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Sensitive information             | Detects files that contain sensitive information in images.                                                                                                                                                      |
|                                   |                                                                                                                                                                                                                  |
|                                   | -  The paths that are not checked by default are as follows:                                                                                                                                                     |
|                                   |                                                                                                                                                                                                                  |
|                                   |    -  /usr/\*                                                                                                                                                                                                    |
|                                   |    -  /lib/\*                                                                                                                                                                                                    |
|                                   |    -  /lib32/\*                                                                                                                                                                                                  |
|                                   |    -  /bin/\*                                                                                                                                                                                                    |
|                                   |    -  /sbin/\*                                                                                                                                                                                                   |
|                                   |    -  /var/lib/\*                                                                                                                                                                                                |
|                                   |    -  /var/log/\*                                                                                                                                                                                                |
|                                   |    -  *Any path*/node_modules/*any path*/*any name*.md                                                                                                                                                           |
|                                   |    -  *Any path*/node_modules/*any path*/test/*any path*                                                                                                                                                         |
|                                   |    -  \*/service/iam/examples_test.go                                                                                                                                                                            |
|                                   |    -  *Any path*/grafana/public/build/*any name*.js                                                                                                                                                              |
|                                   |                                                                                                                                                                                                                  |
|                                   |    .. note::                                                                                                                                                                                                     |
|                                   |                                                                                                                                                                                                                  |
|                                   |       -  Any path: indicates that the current path is a customized value and can be any path in the system.                                                                                                      |
|                                   |       -  Any name: indicates that the file name in the current path is a customized value, which can be any name ended with .md or .js in the system.                                                            |
|                                   |       -  On the **View Report** > **Sensitive Information** tab, click **Configure Sensitive File Path** to set the Linux path of the file that does not need to be checked. A maximum of 20 paths can be added. |
|                                   |                                                                                                                                                                                                                  |
|                                   | -  No checks are performed in the following scenarios:                                                                                                                                                           |
|                                   |                                                                                                                                                                                                                  |
|                                   |    -  The file size is greater than 20 MB.                                                                                                                                                                       |
|                                   |    -  The file type can be binary, common process, or auto generation.                                                                                                                                           |
+-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Software compliance               | Detects software and tools that are not allowed to be used.                                                                                                                                                      |
+-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Basic image information           | Detects service images that are not created using base images.                                                                                                                                                   |
+-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Log in to the management console and go to the HSS page.
#. In the navigation pane, choose **Asset Management** > **Containers & Quota**.
#. Click the **Container Images** tab and select **Private images**. In the **Operation** column of an image, click **Scan**.
#. In the displayed dialog box, click **OK** to start the scan job.
#. **Scanned** in the **Scan Status** column indicates the target image scan completed.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

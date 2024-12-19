:original_name: hss_01_0299.html

.. _hss_01_0299:

Managing SWR Private Images
===========================

Images in the private image repository come from SWR images. You can manually scan for and check reports on vulnerabilities, malicious files, software information, file information, baseline check, and sensitive information.

Constraints
-----------

-  Only the HSS container edition supports this function.

-  Security scans can be performed only on Linux images.

Viewing SWR Private Images
--------------------------

#. Log in to the management console.
#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.
#. In the navigation pane, choose **Asset Management** > **Containers & Quota**.
#. Click the **Container Images** tab and click **SWR private image**.
#. You can click **Update Private Images from SWR** to update private images from SWR.

Scanning an SWR Private Image
-----------------------------

You can choose all images, multiple images, or a single image and manually start a scan. The duration of a security scan depends on the scanned image size. Generally, scanning an image takes shorter than 3 minutes. After the scan is complete, click **View Report** to check the report.

Scan items of private images in SWR are as follows:

+-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Scan Item                         | Description                                                                                                                                                                                                     |
+===================================+=================================================================================================================================================================================================================+
| Vulnerability                     | Detects system and application vulnerabilities in images.                                                                                                                                                       |
+-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Malicious file                    | Detects malicious files in images.                                                                                                                                                                              |
+-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Software information              | Collects software information in an image.                                                                                                                                                                      |
+-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| File information                  | Collects file information in an image.                                                                                                                                                                          |
+-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Unsafe setting                    | -  Configuration check:                                                                                                                                                                                         |
|                                   |                                                                                                                                                                                                                 |
|                                   |    -  Checks the images configurations of CentOS 7, Debian 10, EulerOS, and Ubuntu16.                                                                                                                           |
|                                   |    -  Checks SSH configurations.                                                                                                                                                                                |
|                                   |                                                                                                                                                                                                                 |
|                                   | -  Weak password check: detects weak passwords in images.                                                                                                                                                       |
|                                   | -  Password complexity check: detects insecure password complexity policies in images.                                                                                                                          |
+-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Sensitive information             | Detects files that contain sensitive information in images.                                                                                                                                                     |
|                                   |                                                                                                                                                                                                                 |
|                                   | -  The paths that are not checked by default are as follows:                                                                                                                                                    |
|                                   |                                                                                                                                                                                                                 |
|                                   |    -  /usr/\*                                                                                                                                                                                                   |
|                                   |    -  /lib/\*                                                                                                                                                                                                   |
|                                   |    -  /lib32/\*                                                                                                                                                                                                 |
|                                   |    -  /bin/\*                                                                                                                                                                                                   |
|                                   |    -  /sbin/\*                                                                                                                                                                                                  |
|                                   |    -  /var/lib/\*                                                                                                                                                                                               |
|                                   |    -  /var/log/\*                                                                                                                                                                                               |
|                                   |    -  *AnyPath*/node_modules/*AnyPath*/*AnyName*.md                                                                                                                                                             |
|                                   |    -  *AnyPath*/node_modules/*AnyPath*/test/*AnyPath*                                                                                                                                                           |
|                                   |    -  \*/service/iam/examples_test.go                                                                                                                                                                           |
|                                   |    -  *AnyPath*/grafana/public/build/*AnyName*.js                                                                                                                                                               |
|                                   |                                                                                                                                                                                                                 |
|                                   |    .. note::                                                                                                                                                                                                    |
|                                   |                                                                                                                                                                                                                 |
|                                   |       -  *AnyPath*: indicates that the current path is a customized value and can be any path in the system.                                                                                                    |
|                                   |       -  *AnyName*: indicates that the file name in the current path is a customized value, which can be any name ended with .md or .js in the system.                                                          |
|                                   |       -  On the **View Report** > **Sensitive Information** tab, click **Configure Sensitive File Path** to set the Linux paths of the file that do not need to be checked. A maximum of 20 paths can be added. |
|                                   |                                                                                                                                                                                                                 |
|                                   | -  No checks are performed in the following scenarios:                                                                                                                                                          |
|                                   |                                                                                                                                                                                                                 |
|                                   |    -  The file size is greater than 20 MB.                                                                                                                                                                      |
|                                   |    -  The file type can be binary, common process, or auto generation.                                                                                                                                          |
+-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Software compliance               | Detects software and tools that are not allowed to be used.                                                                                                                                                     |
+-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Basic image information           | Detects service images that are not created using base images.                                                                                                                                                  |
+-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Log in to the management console and go to the HSS page.
#. In the navigation pane, choose **Asset Management** > **Containers & Quota**.
#. In the **Operation** column of an image, click **Scan**.
#. Click the **Container Images** tab and click **SWR private image**.
#. Perform a security scan for a single image or multiple images.

   -  Single image security scan

      In the **Operation** column of the target image, click **Scan** to perform security scan.

   -  Batch image security scan

      Select all target images and click **Scan** above the image list to perform security scan for multiple target images.

   -  Full image security scan

      Click **Scan All** above the image list to perform a security scan for all images.

#. In the displayed dialog box, click **OK** to start the scan job.
#. **Scanned** in the **Scan Status** column indicates the target image scan completed.

Checking the Security Reports of SWR Private Images
---------------------------------------------------

After the scanning is complete, you can view the security reports.

#. Log in to the management console and go to the HSS page.

#. In the navigation pane, choose **Asset Management** > **Containers & Quota**.

#. Click the **Container Images** tab and click and click **Private Images (SWR)**.Click **View Report** in the **Operation** column. The security report details page is displayed.

#. Check the SWR private image security report. For more information, see :ref:`Table 1 <hss_01_0299__table19323150203918>`.

   .. _hss_01_0299__table19323150203918:

   .. table:: **Table 1** Security report parameters

      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                                          |
      +===================================+======================================================================================================================================================================================+
      | Basic Information                 | Displays basic image information, including the image names, organizations, image tags, image sizes, number of vulnerabilities, last update time of the image tags, and scan status. |
      |                                   |                                                                                                                                                                                      |
      |                                   | To rescan image security, click **Scan Again**.                                                                                                                                      |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Vulnerability Reports             | Displays the scan results of image system vulnerabilities and application vulnerabilities.                                                                                           |
      |                                   |                                                                                                                                                                                      |
      |                                   | -  Viewing vulnerability details                                                                                                                                                     |
      |                                   |                                                                                                                                                                                      |
      |                                   |    Click a vulnerability name to go to the vulnerability details page and view the basic information and affected images.                                                            |
      |                                   |                                                                                                                                                                                      |
      |                                   | -  Viewing the **CVE ID**, **CVSS Score**, and **Disclosed Time** of a vulnerability                                                                                                 |
      |                                   |                                                                                                                                                                                      |
      |                                   |    Click |image2| in front of a vulnerability name to view its CVE ID, CVSS score, and the time when it was disclosed.                                                               |
      |                                   |                                                                                                                                                                                      |
      |                                   | -  Viewing vulnerability solutions                                                                                                                                                   |
      |                                   |                                                                                                                                                                                      |
      |                                   |    In the **Solution** column of a vulnerability, click the solution description to view the vulnerability solution details.                                                         |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Malicious Files                   | Displays the scan results of malicious image files, including the malicious file names, paths, and file sizes.                                                                       |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Software Information              | Displays the statistical results of image software information, including the software names, types, versions, and number of software vulnerabilities.                               |
      |                                   |                                                                                                                                                                                      |
      |                                   | Click |image3| next to a software name to view the software vulnerability name, repair urgency, and solution.                                                                        |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | File Information                  | Displays the statistical results of image file information, including the total number of files, total file size, and details about the top 50 files.                                |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Unsafe Settings                   | Displays the image baseline check results, including the configuration check, password complexity policy check, and common weak password check results.                              |
      |                                   |                                                                                                                                                                                      |
      |                                   | -  Viewing unsafe settings and suggestions                                                                                                                                           |
      |                                   |                                                                                                                                                                                      |
      |                                   |    a. On the **Unsafe Configurations** tab page, select a baseline.                                                                                                                  |
      |                                   |    b. In the detection item column of a detection item, click **Description** to view the detection item description and modification suggestions.                                   |
      |                                   |                                                                                                                                                                                      |
      |                                   | -  Customizing common weak passwords                                                                                                                                                 |
      |                                   |                                                                                                                                                                                      |
      |                                   |    a. Click **Common Weak Password Detection**.                                                                                                                                      |
      |                                   |    b. Configure weak passwords and click **OK**.                                                                                                                                     |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Sensitive Information             | Displays the scan result of sensitive image information, including the risk levels, image paths, file paths, and sensitive information.                                              |
      |                                   |                                                                                                                                                                                      |
      |                                   | To add the paths of sensitive files that are not detected, choose **Configure Sensitive File Path** and add the paths to be filtered.                                                |
      |                                   |                                                                                                                                                                                      |
      |                                   | -  Only Linux system file paths can be filtered.                                                                                                                                     |
      |                                   | -  A maximum of 20 paths can be added. Put each path on a separate line.                                                                                                             |
      |                                   | -  Example: **/usr/** or **/lib/test.txt**.                                                                                                                                          |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Software Compliance               | Displays the scan results of non-compliant image software, including the non-compliant software name, path, and image layer information.                                             |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Base Images                       | Displays the scan results of service images that are not built using basic images. The scan results include image names, versions, and image paths.                                  |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Exporting a Private Image Vulnerability Report
----------------------------------------------

#. Log in to the management console and go to the HSS page.
#. In the navigation pane, choose **Asset Management** > **Containers & Quota**.

3. Click the **Container Images** tab and click **Private Images (SWR)**.

4. Click **Export Vulnerability** above the image list and select a report type to export the vulnerability or baseline report.

   If you want to export the vulnerability report of a specified image, select the image type in the search box and click **Export Vulnerability**.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png
.. |image2| image:: /_static/images/en-us_image_0000001974048962.png
.. |image3| image:: /_static/images/en-us_image_0000001973906080.png

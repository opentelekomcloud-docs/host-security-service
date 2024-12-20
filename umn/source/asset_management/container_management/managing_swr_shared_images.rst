:original_name: hss_01_0088.html

.. _hss_01_0088:

Managing SWR Shared Images
==========================

The images in the shared image repository are from SWR. You can view details about all shared images.

Constraints
-----------

-  Only the HSS container edition supports this function.

-  Security scans can be performed only on Linux images.

Viewing SWR Shared Images
-------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane, choose **Asset Management** > **Containers & Quota**.

   .. note::

      If your servers are managed by enterprise projects, you can select the target enterprise project to view or operate the asset and detection information.

#. Click the **Container Images** tab and click **SWR shared image** to view the shared image list.

   You can view the version, size, organization, security risks, and owner of a shared image.


   .. figure:: /_static/images/en-us_image_0000002051201908.png
      :alt: **Figure 1** Viewing shared images

      **Figure 1** Viewing shared images

   -  Updating a shared image

      Click **Update Shared Images from SWR** to update the shared image list.

   -  Filtering images of the latest version

      If you select **Display latest image versions only**, you can filter the latest images of all images.

Scanning SWR Shared Images
--------------------------

You can manually scan SWR shared images in the **Valid** state. The duration of a security scan depends on the image size. Generally, an image can be scanned within 3 minutes. After the scan is complete, click **View Report** to view the security report.

The following scan items are supported.

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

2. In the navigation pane, choose **Asset Management** > **Containers & Quota**.

   .. note::

      If your servers are managed by enterprise projects, you can select the target enterprise project to view or operate the asset and detection information.

3. Click the **Container Images** tab and click **SWR shared image**.
4. Performs a security scan for a single image or multiple images.

   .. note::

      You can perform a security scan only when the status is **Valid**.

   -  Single image security scan

      In the **Operation** column of the target image, click **Scan** to perform security scan.

   -  Batch image security scan

      Select all target images and click **Scan** above the image list to perform security scan for multiple target images.

   -  Full image security scan

      Click **Scan All** above the image list to perform a security scan for all images.

5. The image security scan is complete, when the **Scan Status** changes to **Completed** and the **Latest Scan Completed** shows the latest task execution time.

Checking the Security Reports of SWR Shared Images
--------------------------------------------------

After the scanning is complete, you can view the security reports.

#. Log in to the management console and go to the HSS page.

2. In the navigation pane, choose **Asset Management** > **Containers & Quota**.

3. Click the **Container Images** tab and click **SWR shared image**.

4. In the **Operation** column of the target image, click **View Report**. The security scan report page is displayed.

5. Check the SWR shared image security report. For more information, see :ref:`Table 1 <hss_01_0088__table19323150203918>`.

   .. _hss_01_0088__table19323150203918:

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
      |                                   | -  Common weak password detection                                                                                                                                                    |
      |                                   |                                                                                                                                                                                      |
      |                                   |    a. Click **Common Weak Password Detection**.                                                                                                                                      |
      |                                   |    b. Configure weak passwords and click **OK**.                                                                                                                                     |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Sensitive Information             | Displays the scan result of sensitive image information, including the risk levels, image paths, file paths, and sensitive information.                                              |
      |                                   |                                                                                                                                                                                      |
      |                                   | -  Prompt for ignoring sensitive information                                                                                                                                         |
      |                                   |                                                                                                                                                                                      |
      |                                   |    In the **Operation** column of the target sensitive information file, click **Ignore** to ignore the sensitive information that you think is secure.                              |
      |                                   |                                                                                                                                                                                      |
      |                                   | -  Adding a sensitive file path                                                                                                                                                      |
      |                                   |                                                                                                                                                                                      |
      |                                   |    To add the paths of sensitive files that are not detected, choose **Configure Sensitive File Path** and add the paths to be filtered.                                             |
      |                                   |                                                                                                                                                                                      |
      |                                   |    -  Only Linux system file paths can be filtered.                                                                                                                                  |
      |                                   |    -  A maximum of 20 paths can be added. Put each path on a separate line.                                                                                                          |
      |                                   |    -  Example: **/usr/** or **/lib/test.txt**.                                                                                                                                       |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Software Compliance               | Displays the scan results of non-compliant image software, including the non-compliant software name, path, and image layer information.                                             |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Base Images                       | Displays the scan results of service images that are not built using basic images. The scan results include image names, versions, and image paths.                                  |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Exporting the SWR Shared Image Vulnerability Report
---------------------------------------------------

#. Log in to the management console and go to the HSS page.

2. In the navigation pane, choose **Asset Management** > **Containers & Quota**.

3. Click the **Container Images** tab and click **SWR shared image**.

4. Click **Export Vulnerability** above the image list and select a report type to export the vulnerability or baseline report.

   If you want to export the vulnerability report of a specified image, select the image type in the search box and click **Export Vulnerability**.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png
.. |image2| image:: /_static/images/en-us_image_0000002010847789.png
.. |image3| image:: /_static/images/en-us_image_0000001974207582.png

:original_name: hss_01_0297.html

.. _hss_01_0297:

Managing Local Images
=====================

You can manually scan local images for vulnerabilities and software information and provides scan reports. This section describes how to perform security scans on local images and view scan reports.

Constraints
-----------

-  Only the HSS container edition supports this function.

-  Only the local images of the Docker engine can be reported to the HSS console.
-  Security scans can be performed only on Linux images.
-  Only the images whose storage drive is OverlayFS or OverlayFS2 can be scanned. Nodes using Device Mapper cannot be scanned.
-  Images whose names or versions are **--** cannot be scanned.
-  HSS only has the permission to access the default scan directory **/var/run**. If **Docker Root Dir** is not **/var/run/**, HSS cannot scan images. You are advised to perform image scanning on the Containerd server.

Viewing Local Images
--------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane, choose **Asset Management** > **Containers & Quota**. Click the **Container Images** tab and click **Local image** to view local images.


   .. figure:: /_static/images/en-us_image_0000002087200905.png
      :alt: **Figure 1** Viewing the local image scan results

      **Figure 1** Viewing the local image scan results

Scanning Local Images
---------------------

The following security scan items are supported for local images:

================== ==========================================
Scan Item          Description
================== ==========================================
Vulnerability      Detects vulnerabilities in images.
Installed software Collects software information in an image.
================== ==========================================

#. Log in to the management console and go to the HSS page.
#. In the navigation pane, choose **Asset Management** > **Containers & Quota**.
#. Click the **Container Images** tab and click **Local image**.
#. Performs a security scan for a single image or multiple images.

   -  Single image security scan

      In the **Operation** column of the target image, click **Scan** to perform security scan.

   -  Batch image security scan

      Select all target images and click **Scan** above the image list to perform security scan for multiple target images.

   -  Full image security scan

      Click **Scan All** above the image list to perform a security scan for all images.

#. The image security scan is complete, when the **Scan Status** changes to **Completed** and the **Latest Scan Completed** shows the latest task execution time.

Viewing Local Image Vulnerability Reports and Software Information
------------------------------------------------------------------

#. Log in to the management console and go to the HSS page.

#. In the navigation pane, choose **Asset Management** > **Containers & Quota**. Click the **Container Images** tab and click **Local image** to view local images.


   .. figure:: /_static/images/en-us_image_0000002087200905.png
      :alt: **Figure 2** Viewing the local image scan results

      **Figure 2** Viewing the local image scan results

#. Click **View Report** in the **Operation** column of the target image to view the basic information, vulnerability report, and software information about the image.

Exporting Local Image Vulnerability Reports
-------------------------------------------

#. Log in to the management console and go to the HSS page.

2. In the navigation pane, choose **Asset Management** > **Containers & Quota**.

3. Click the **Container Images** tab and click **Local image**.

4. Click **Export Vulnerability** above the image list.

   If you want to export the vulnerability report of a specified image, select the image type in the search box and click **Export Vulnerability**.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

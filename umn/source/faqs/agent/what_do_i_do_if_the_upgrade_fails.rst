:original_name: hss_01_0409.html

.. _hss_01_0409:

What Do I Do If the  Upgrade Fails?
===================================

About the Upgrade
-----------------

-  Servers are displayed on both the old and new console of HSS, regardless of whether their agents have been upgraded. The server statuses are properly displayed on the console that you are using.
-  Agent upgrade is free of charge.
-  The upgrade does not affect the workloads on your cloud servers.
-  After the upgrade, the billing stops on the old console and starts on the new console.
-  After the upgrade, your servers will be protected by HSS (New).

Possible Causes
---------------

.. note::

   After the automatic upgrade is complete, it takes 5 to 10 minutes for the agent status to be refreshed.

Possible causes for abnormal agent statuses are as follows:

#. Access to port 10180 is restricted. The agent upgrade requires accessed to port 10180.
#. The available memory of the server is insufficient. The agent upgrade occupies certain memory. If the available memory is less than 300 MB, the upgrade will be affected.

Locating and Fixing the Problem
-------------------------------

-  **Restricted Access to Port 10180**

   Ensure the server where the agent is to be installed or upgraded can communicate with the network segment. The security group of your server must allow outbound access to port 10180 on the 100.125.X.X/16 network segment.

   -  Troubleshooting Procedure

      #. In the upper left corner of the page, select a region, click |image1|, and choose **Compute** > **Elastic Cloud Server**.
      #. Click the name of the server. On the server details page that is displayed, click the **Security Groups** tab.
      #. Click the **Outbound Rules** tab and check whether port 10180 is specified in the deny policy.

         a. If it is not specified, the problem was not caused by port access restriction.
         b. If it is specified, the problem was caused by port access restriction.

   -  Solution

      Allow access to the port.

-  **The available memory is insufficient.**

   -  Troubleshooting Procedure

      -  Linux

         #. Use a remote management tool, such as SecureFX or WinSCP, to log in to the server.

         #. Run the following command to check the memory usage of the server:

            free -m

         #. Check the value of **free** in the command output, as shown in :ref:`Figure 1 <hss_01_0409__fig172244311447>`.

            If the value of **available** is smaller than 300, the memory is insufficient.

            .. _hss_01_0409__fig172244311447:

            .. figure:: /_static/images/en-us_image_0000001517158254.png
               :alt: **Figure 1** Querying the memory

               **Figure 1** Querying the memory

      -  Windows

         #. Use a remote management tool, such as mstsc and RDP, to log in to the server.

         #. Open the Task Manager.

         #. Choose **Performance** > **Memory**, and view the available memory on the **Memory** page.

            If the available memory is less than 300 MB, the memory is insufficient.

   -  Solution

      -  Close the applications with high memory usage.

.. |image1| image:: /_static/images/en-us_image_0000001517637374.png

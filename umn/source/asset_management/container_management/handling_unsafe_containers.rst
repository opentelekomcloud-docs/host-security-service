:original_name: hss_01_0506.html

.. _hss_01_0506:

Handling Unsafe Containers
==========================

Scenario
--------

HSS can detect container security risks and classify them into the following types:

-  Critical: malicious program
-  High risk: ransomware attacks, malicious programs, reverse shells, escape attacks, and dangerous commands
-  Medium risk: web shell, abnormal startup, process exception, and sensitive file access
-  Low risk: brute-force attack

To prevent containers with medium or higher security risks from affecting other containers, you can isolate, suspend, or stop risky containers.

Constraints
-----------

-  Only the HSS container edition supports this function.
-  Only Linux containers are supported.
-  Only containers with medium or higher security risks can be handled.


Handling Unsafe Containers
--------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane, choose **Asset Management** > **Containers & Quota**.

#. Choose **Containers**. The container page is displayed.

#. Enter **Risk** in the search box and click |image2| to filter containers with security risks.

#. In the **Operation** column of the target risky container, select the operation to be performed.

   Cluster containers can be stopped. Independent containers can be isolated, suspended, and stopped.

   .. note::

      Only containers with medium or higher risks can be handled. You can view the security risk distribution.

   -  **Isolate containers**: After a container is isolated, you cannot access the container when the container is running, and the container cannot access the mount directory of the host or the system file of the container.

      a. Click **Isolate**.
      b. In the dialog box that is displayed, click **OK**.

   -  **Suspend containers**: Freeze the processes running in the container.

      a. Click **Suspend**.
      b. In the dialog box that is displayed, click **OK**.

   -  **Stop containers**: Terminate a running container process. If **autoremove** is configured for the container, the container cannot be resumed.

      a. Click **Stop Container**.
      b. In the dialog box that is displayed, click **OK**.

Related Operations
------------------

**Restoring a container to the running state**

Restores a container from the **Isolate**, **Waiting**, or **Terminated** state to the **Running** state.

.. note::

   If **autoremove** is configured for a terminated container, the container cannot be resumed.

#. In the row containing the target container, click **Restore** in the **Operation** column.
#. In the dialog box that is displayed, click **OK**.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png
.. |image2| image:: /_static/images/en-us_image_0000001632965461.png

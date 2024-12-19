:original_name: hss_01_0630.html

.. _hss_01_0630:

Container Cluster Protection Overview
=====================================

HSS can check for non-compliance baseline issues, vulnerabilities, and malicious files when a container image is started and report alarms on or block container startup that has not been unauthorized or may incur high risks.

You can configure container cluster protection policies to block images with vulnerabilities, malicious files, non-compliant baselines, or other threats, hardening cluster security.

Constraints and Limitations
---------------------------

-  Container cluster protection is available only in the HSS container edition.
-  To use container cluster protection, ensure the agent installed on the server falls within the following range. For details about how to upgrade the agent, see :ref:`Upgrading the Agent <hss_01_0462>`.

   -  Linux: 3.2.7 or later
   -  Windows: 4.0.19 or later

Process of Using Container Cluster Protection
---------------------------------------------


.. figure:: /_static/images/en-us_image_0000001929146205.png
   :alt: **Figure 1** Usage process

   **Figure 1** Usage process

.. table:: **Table 1** Process of using container cluster protection

   +-----------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Operation                                                       | Description                                                                                                                                                                               |
   +=================================================================+===========================================================================================================================================================================================+
   | :ref:`Enable container cluster protection. <hss_01_0631>`       | Enable protection for a cluster to protect its workloads and critical data. When protection is enabled, HSS automatically installs the policy management plug-in on the cluster.          |
   +-----------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`Configure a protection policy. <hss_01_0632>`             | Configure the severity of baseline, vulnerability, and malicious file risks that trigger alarms; container cluster protection scope; image whitelist; and actions to be taken on alarms.  |
   +-----------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`Check container cluster protection events. <hss_01_0633>` | On the HSS console, you can view unauthorized or high-risk container image running events that are reported or blocked, and check and clear insecure container images in a timely manner. |
   +-----------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

:original_name: hss_01_0037.html

.. _hss_01_0037:

Is the Agent in Conflict with Any Other Security Software?
==========================================================

Yes, it may be in conflict with DenyHosts.

-  Symptom: The IP address of the login host is identified as an attack IP address but can not be unblocked.
-  Cause: HSS and DenyHosts both block possible attack IP addresses, but HSS can not unblock the IP addresses that were blocked by DenyHosts.
-  Handling method: Stop DenyHosts.
-  Procedure

   #. Log in as user **root** to ECS.

   #. Run the following command to check whether DenyHosts has been installed:

      **ps -ef \| grep denyhosts.py**

      If information similar to the following is displayed, DenyHosts has been installed:

      |image1|

   #. Run the following command to stop DenyHosts:

      **kill -9 'cat /var/lock/denyhosts'**

   #. Run the following command to cancel the automatic start of DenyHosts upon host startup:

      **chkconfig --del denyhosts;**

.. |image1| image:: /_static/images/en-us_image_0000001517317850.png

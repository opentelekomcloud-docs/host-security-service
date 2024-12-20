:original_name: hss_01_0512.html

.. _hss_01_0512:

What Do I Do If the Port in Brute-force Attack Records Is Not Updated?
======================================================================

Symptom
-------

The remote port of a server has been changed, but the brute-force attack records still displays the old port.

Solution
--------

The remote port configuration is synchronized to HSS through the agent. If the remote port is changed, perform the following operations to restart the agent:

-  Windows: Log in to the server as an administrator. Open Task Manager, right-click **HostGuard** and choose **Restart** from the shortcut menu.
-  Linux: Run the **service hostguard restart** command as the **root** user.

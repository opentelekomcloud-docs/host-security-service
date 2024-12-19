:original_name: hss_01_0394.html

.. _hss_01_0394:

What Can I Do If the Agent Status Is Still "Not installed" After Installation?
==============================================================================

Precautions
-----------

On a server, you only need to install the agent once.

After the installation, you are advised to restart the servers before enabling HSS and binding quotas.

Possible Cause
--------------

Now both the HSS (New) and HSS (Old) consoles are in use. The agent and protection statuses of a server can be properly displayed on only one of the consoles.

For example, if you have installed the agent on server A on the old console and try installing it again on the new console, a message will be displayed indicating the installation has succeeded, but the installation status on the new console will still be **Not installed**.

Solution
--------

Use only one console. Do not switch between the old and new consoles.

If you are using the old console and the agent status is **Not installed** on the new console, you can upgrade the agent to use HSS (New). The upgrade is free of charge and does not affect services. After the upgrade, the agent is installed on the new console, and the agent status is **Not installed** on the old console.

.. note::

   HSS (New) added application protection capabilities, which are not available in the old version. You are advised to use the new version.

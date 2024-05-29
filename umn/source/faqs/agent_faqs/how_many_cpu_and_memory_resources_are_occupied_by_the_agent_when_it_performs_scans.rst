:original_name: hss_01_0116.html

.. _hss_01_0116:

How Many CPU and Memory Resources Are Occupied by the Agent When It Performs Scans?
===================================================================================

HSS uses lightweight agents, which occupy only a few resources and do not affect your services.

The CPU and memory usage is as follows.

Maximum CPU Usage
-----------------

A running agent occupies a maximum of 20% of a vCPU. The actual usage depends on your server specifications. For details, see :ref:`Resource Usage of Different Specifications While the Agent Is Running <hss_01_0116__section08751730152715>`.

If the CPU usage exceeds 20% of a vCPU, the agent will automatically reduce CPU usage, spending more time on scans. This does not affect your services. If the CPU usage exceeds 25% of a vCPU, the agent will be automatically restarted.

.. note::

   The agent is scheduled to scan your servers from 00:00 to 04:00 a.m. local server time every day. It does not affect the normal running of the server system.

Peak Memory Usage
-----------------

A running agent occupies about **500 MB** memory. If the agent memory usage exceeds the maximum memory limit **500 MB**, the agent will be automatically restarted within 5 minutes.

.. _hss_01_0116__section08751730152715:

Resource Usage of Different Specifications While the Agent Is Running
---------------------------------------------------------------------

The following table describes the CPU and memory usage of different specifications when the agent is running.

.. table:: **Table 1** Resource usage of the agent

   ======== ======================= =================
   vCPUs    Max. CPU Usage of Agent Max. Memory Usage
   ======== ======================= =================
   1 vCPU   20%                     500 MB
   2 vCPUs  10%                     500 MB
   4 vCPUs  5%                      500 MB
   8 vCPUs  2.5%                    500 MB
   12 vCPUs About 1.67%             500 MB
   16 vCPUs About 1.25%             500 MB
   24 vCPUs About 0.84%             500 MB
   32 vCPUs About 0.63%             500 MB
   48 vCPUs About 0.42%             500 MB
   60 vCPUs About 0.34%             500 MB
   64 vCPUs About 0.32%             500 MB
   ======== ======================= =================

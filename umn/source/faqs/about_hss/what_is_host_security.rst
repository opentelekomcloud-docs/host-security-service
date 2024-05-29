:original_name: hss_01_0033.html

.. _hss_01_0033:

What Is Host Security?
======================

Host Security Service (HSS) helps you identify and manage the assets on your servers, eliminate risks, and defend against intrusions and web page tampering. There are also advanced protection and security operations functions available to help you easily detect and handle threats.

How HSS Works
-------------

Install the HSS agent on your servers, and you will be able to check the server security status and risks in a region on the HSS console.

:ref:`Figure 1 <hss_01_0033__en-us_topic_0000001124699553_fig350352519269>` shows the working principles of HSS.

.. _hss_01_0033__en-us_topic_0000001124699553_fig350352519269:

.. figure:: /_static/images/en-us_image_0000001687084998.png
   :alt: **Figure 1** Working principles

   **Figure 1** Working principles

The functions and working processes of HSS components are described as follows:

.. table:: **Table 1** Components

   +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Component                         | Description                                                                                                                                                                                                                                                                                     |
   +===================================+=================================================================================================================================================================================================================================================================================================+
   | Management console                | A visualized management platform, where you can apply configurations in a centralized manner and view the protection status and scan results of servers in a region.                                                                                                                            |
   +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | HSS cloud protection center       | -  Analyzes security risks in servers using AI, machine learning, and deep learning algorithms.                                                                                                                                                                                                 |
   |                                   | -  Integrates multiple antivirus engines to detect and kill malicious programs in servers.                                                                                                                                                                                                      |
   |                                   | -  Receives configurations and scan tasks sent from the console and forwards them to agents on the servers.                                                                                                                                                                                     |
   |                                   | -  Receives server information reported by agents, analyzes security risks and exceptions on servers, and displays the analysis results on the console.                                                                                                                                         |
   +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Agent                             | -  Communicates with the HSS cloud protection center via HTTPS and WSS. Port 10180 is used by default.                                                                                                                                                                                          |
   |                                   | -  Scans all servers every early morning; monitors the security status of servers; and reports the collected server information (including non-compliant configurations, insecure configurations, intrusion traces, software list, port list, and process list) to the cloud protection center. |
   |                                   | -  Blocks server attacks based on the security policies you configured.                                                                                                                                                                                                                         |
   |                                   |                                                                                                                                                                                                                                                                                                 |
   |                                   | .. note::                                                                                                                                                                                                                                                                                       |
   |                                   |                                                                                                                                                                                                                                                                                                 |
   |                                   |    -  If no agent is installed or the agent installed is abnormal, the HSS is unavailable.                                                                                                                                                                                                      |
   |                                   |    -  Select the agent and installation command suitable for your OS.                                                                                                                                                                                                                           |
   |                                   |    -  The HSS agent can be used for all editions, including container security and Web Tamper Protection (WTP). You only need to install the agent once on the same server.                                                                                                                     |
   +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

:original_name: hss_01_0001.html

.. _hss_01_0001:

What Is HSS?
============

HSS is designed to protect server workloads in hybrid clouds and multi-cloud data centers. It provides host security functions, Container Guard Service (CGS), and Web Tamper Protection (WTP).

HSS can help you remotely check and manage your servers and containers in a unified manner.

HSS protects your system integrity, enhances application security, monitors user operations, and detects intrusions.

Host Security
-------------

Host Security Service (HSS) helps you identify and manage the assets on your servers, eliminate risks, and defend against intrusions and web page tampering. There are also advanced protection and security operations functions available to help you easily detect and handle threats.

Install the HSS agent on your servers, and you will be able to check the server protection status and risks in a region on the HSS console.

:ref:`Figure 1 <hss_01_0001__fig350352519269>` illustrates how HSS works.

.. _hss_01_0001__fig350352519269:

.. figure:: /_static/images/en-us_image_0000001687084998.png
   :alt: **Figure 1** Working principles

   **Figure 1** Working principles

The following table describes the HSS components.

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

Container Security
------------------

HSS provides container security capabilities. The agent deployed on a server can scan the container images on the server, checking configurations, detecting vulnerabilities, and uncovering runtime issues that cannot be detected by traditional security software. Container security also provides functions such as process whitelist, read-only file protection, and container escape detection to minimize the security risks for a running container.

Web Tamper Protection
---------------------

Web Tamper Protection (WTP) monitors website directories in real time and restores tampered files and directories using their backups. It protects website information, such as web pages, electronic documents, and images, from being tampered with or damaged by hackers.


.. figure:: /_static/images/en-us_image_0000001517477602.jpg
   :alt: **Figure 2** How WTP works

   **Figure 2** How WTP works

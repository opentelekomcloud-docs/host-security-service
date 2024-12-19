:original_name: hss_01_0491.html

.. _hss_01_0491:

Plug-Ins Overview
=================

If container protection is enabled and you want to use the image blocking function, you need to :ref:`install the Docker plug-in <hss_01_0481>`.

The Docker plug-in provides the image blocking capability. It can prevent the startup of container images that have high-risk vulnerabilities or do not comply with security standards in the Docker environment.

You can configure image blocking in the following scenarios:

-  To enhance the security of container images and prevent the risks caused by the use of untrusted or outdated images, you can configure an :ref:`image blocking policy <hss_01_0044__section1718012455468>` to specify the level of vulnerabilities to be blocked or the whitelist.
-  If you need to comply with the security requirements of certain industries or regulations, such as PCI DSS and CIS, you can :ref:`configure an image blocking policy <hss_01_0044__section1718012455468>` to specify the security baseline or compliance check items to be blocked.
-  If you need to implement the best practices of container DevSecOps and embed security check and defense into each phase of the container lifecycle, you can :ref:`configure an image blocking policy <hss_01_0044__section1718012455468>` to enhance security from source to devices.

Constraints and Limitations
---------------------------

The constraints for installing the Docker plug-in are as follows:

-  The HSS container edition has been enabled.
-  Only Docker containers can use this plug-in.
-  The Docker engine version is 18.06.0 or later.
-  The Docker API version is 1.38 or later.
-  Only Linux servers are supported.
-  Only the x86 and Arm hardware architectures are supported.

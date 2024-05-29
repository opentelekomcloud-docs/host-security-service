:original_name: hss_01_0097.html

.. _hss_01_0097:

What Do I Do If the Account Cracking Prevention Function Does Not Take Effect on Some Accounts for Linux Servers?
=================================================================================================================

Possible Causes
---------------

The SSHD service in the host system does not depend on **libwrap.so**.

.. note::

   As a free software library, libwrap implements the universal TCP Wrapper function. Any daemon that contains **libwrap.so** can use the rules in files **/etc/hosts.allow** and **/etc/hosts.deny** to perform simple access control on the host.

Solution
--------

Log in to the server and install the HSS agent. Then run the following command:

**sh /usr/local/hostguard/conf/config_ssh_xinetd.sh**.

Affected Image Versions
-----------------------

-  The following are Gentoo images that have the problem:

   -  Gentoo Linux 17.0 64bit (40 GB)
   -  Gentoo Linux 13.0 64bit (40 GB)

-  The following are OpenSUSE images that have the problem:

   -  OpenSUSE 42.2 64bit (40 GB)
   -  OpenSUSE 13.2 64bit (40 GB)

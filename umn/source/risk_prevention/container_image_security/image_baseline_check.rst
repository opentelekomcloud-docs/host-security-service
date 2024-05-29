:original_name: hss_01_0307.html

.. _hss_01_0307:

Image Baseline Check
====================

Your private image repository is scanned for unsafe configurations and provides suggestions for modifying the configurations, helping you fight intrusions and meet compliance requirements.

Check Frequency
---------------

A comprehensive check is automatically performed by HSS at 04:10 every day.

Prerequisites
-------------

Container protection has been enabled.

Constraints
-----------

Only configuration risks in Linux images can be detected.

Check Items
-----------

-  Accounts with duplicate names or UIDs
-  Non-root accounts whose UIDs are 0
-  Password check in code
-  Accounts with duplicate password hash values
-  Weak password hash algorithms
-  The account password is not empty.
-  Duplicate group names or GIDs
-  Non-privileged account incorrectly included in the privilege group
-  Old "+" entries in the /etc/passwd file
-  Old "+" entries in the /etc/shadow file
-  Old "+" entries in the /etc/group file
-  Ensuring all groups in the /etc/passwd file are in the /etc/group file
-  Unconfigured password validity period
-  Ensuring that the password change dates of all users are past dates.
-  Host trust relationship
-  Preset root-level trust relationship establishment
-  The default group of user **root** is **GID 0**.
-  Members in the shadow group

Procedure
---------

#. Log in to the management console.
#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.
#. In the navigation tree on the left, choose **Prediction** > **Container Images**.
#. Click the **Unsafe Settings** tab to view the unsafe settings in the image.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

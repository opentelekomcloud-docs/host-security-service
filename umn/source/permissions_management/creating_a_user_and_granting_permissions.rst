:original_name: hss_01_0133.html

.. _hss_01_0133:

Creating a User and Granting Permissions
========================================

This section describes IAM's fine-grained permissions management for your HSS resources. With IAM, you can:

-  Create IAM users for employees based on the organizational structure of your enterprise. Each IAM user has their own security credentials, providing access to HSS resources.
-  Grant only the permissions required for users to perform a specific task.
-  Entrust a cloud account or cloud service to perform professional and efficient O&M on your HSS resources.

If your account does not require individual IAM users, skip this chapter.

This section describes the procedure for granting permissions (see :ref:`Figure 1 <hss_01_0133__fig392404973213>`).

Prerequisite
------------

Before authorizing permissions to a user group, you need to know which HSS permissions can be added to the user group. :ref:`Table 1 <hss_01_0133__table1990914124510>` describes the policy details.

.. _hss_01_0133__table1990914124510:

.. table:: **Table 1** System-defined permissions supported by HSS

   +--------------------+---------------------------------------------------+-----------------------+-------------------------------------------------------------------------------+
   | Role/Policy Name   | Description                                       | Type                  | Dependency                                                                    |
   +====================+===================================================+=======================+===============================================================================+
   | HSS Administrator  | HSS administrator, who has all permissions of HSS | System-defined role   | -  It depends on the **Tenant Guest** role.                                   |
   |                    |                                                   |                       |                                                                               |
   |                    |                                                   |                       |    Tenant Guest: A global role, which must be assigned in the global project. |
   +--------------------+---------------------------------------------------+-----------------------+-------------------------------------------------------------------------------+
   | HSS FullAccess     | All HSS permissions                               | System-defined policy | None                                                                          |
   +--------------------+---------------------------------------------------+-----------------------+-------------------------------------------------------------------------------+
   | HSS ReadOnlyAccess | Read-only permission for HSS                      | System-defined policy | None                                                                          |
   +--------------------+---------------------------------------------------+-----------------------+-------------------------------------------------------------------------------+

Authorization Process
---------------------

.. _hss_01_0133__fig392404973213:

.. figure:: /_static/images/en-us_image_0000001568317677.png
   :alt: **Figure 1** Process for granting permissions

   **Figure 1** Process for granting permissions

#. .. _hss_01_0133__li1761173372710:

   Create a user group and assign permissions. On the IAM console, grant the **HSS Administrator** permission.

#. Create a user and add it to the group. On the IAM console, add the user to the group created in :ref:`1 <hss_01_0133__li1761173372710>`.

#. Log in and verify permissions.

   Log in to the HSS console as the created user, and verify that the user only has read permissions for HSS.

   In **Service List** on the console, select any other services (for example, there is only the **HSS Administrator** policy). If a message indicating that the permission is insufficient is displayed, the **HSS Administrator** permission takes effect.

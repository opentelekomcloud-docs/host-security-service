:original_name: hss_01_0130.html

.. _hss_01_0130:

HSS Permissions Management
==========================

If you need to assign different permissions to employees in your enterprise to access your HSS resources, IAM is a good choice for fine-grained permissions management. IAM provides identity authentication, permissions management, and access control, helping you secure the access to your cloud resources.

With IAM, you can use your account to create IAM users for your employees, and assign permissions to the users to control their access to specific resource types. For example, some software developers in your enterprise need to use HSS resources but must not delete them or perform any high-risk operations. To achieve this result, you can create IAM users for the software developers and grant them only the permissions required for using HSS resources.

If your account does not need individual IAM users for permissions management, then you may skip over this chapter.

HSS Permissions
---------------

By default, new IAM users do not have permissions assigned. You need to add a user to one or more groups, and attach permissions policies or roles to these groups. Users inherit permissions from their groups and can perform specified operations on cloud services.

HSS is a project-level service deployed and accessed in specific physical regions. To assign HSS permissions to a user group, specify the scope as region-specific projects and select projects for the permissions to take effect. If **All projects** is selected, the permissions will take effect for the user group in all region-specific projects. When accessing HSS, the users need to switch to a region where they have been authorized to use cloud services.

You can grant permissions by using roles or policies.

-  Roles: A type of coarse-grained authorization mechanism that defines permissions related to user responsibilities. This mechanism provides only a limited number of service-level roles for authorization. Some roles depend other roles to take effect. When you assign such roles to users, remember to assign the roles they depend on. However, roles are not an ideal choice for fine-grained authorization and secure access control.
-  Policies: A type of fine-grained authorization that defines permissions required to perform operations on specific cloud resources under certain conditions. This type of authorization is more flexible and ideal for secure access control. For example, you can grant HSS users only the permissions for managing a certain type of resources.

The following table describes more details.

.. table:: **Table 1** System-defined permissions supported by HSS

   +-------------------+---------------------------------------------------+---------------------+-------------------------------------------------------------------------------+
   | Role/Policy Name  | Description                                       | Type                | Dependency                                                                    |
   +===================+===================================================+=====================+===============================================================================+
   | HSS Administrator | HSS administrator, who has all permissions of HSS | System-defined role | -  It depends on the **Tenant Guest** role.                                   |
   |                   |                                                   |                     |                                                                               |
   |                   |                                                   |                     |    Tenant Guest: A global role, which must be assigned in the global project. |
   +-------------------+---------------------------------------------------+---------------------+-------------------------------------------------------------------------------+
   | HSSFullAccess     | All HSS permissions                               | Policy              | None                                                                          |
   +-------------------+---------------------------------------------------+---------------------+-------------------------------------------------------------------------------+
   | HSSReadOnlyAccess | Read-only permission for HSS                      | Policy              | None                                                                          |
   +-------------------+---------------------------------------------------+---------------------+-------------------------------------------------------------------------------+

WTP provides two types of user permissions by default: user management and resource management. User management permissions include permissions for managing users, user groups, and user group permissions. Resource management permissions include permissions for performing operations on cloud resources.

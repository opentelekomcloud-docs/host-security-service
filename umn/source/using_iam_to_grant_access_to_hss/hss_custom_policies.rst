:original_name: hss_01_0005.html

.. _hss_01_0005:

HSS Custom Policies
===================

Custom policies can be created to supplement the system-defined policies of HSS.

You can create custom policies using one of the following methods:

-  Visual editor: Select cloud services, actions, resources, and request conditions. You do not need to have knowledge of the policy syntax.
-  JSON: Create a policy in JSON format or edit the JSON strings of an existing policy.

For details, see "Creating a Custom Policy" in *Identity and Access Management User Guide*. The following section contains examples of common HSS custom policies.

Example Custom Policies
-----------------------

-  Example 1: Allowing users to query the protected server list

   .. code-block::

      {
              "Version": "1.1",
              "Statement": [
                      {
                              "Effect": "Allow",
                              "Action": [
                                      "hss:hosts:list"
                                                             ]
                      }
              ]
      }

-  Example 2: Denying agent uninstallation

   A deny policy must be used together with other policies. If the policies assigned to a user contain both "Allow" and "Deny", the "Deny" permissions take precedence over the "Allow" permissions.

   The following method can be used if you need to assign permissions of the **HSS Administrator** policy to a user but also forbid the user from deleting key pairs (**hss:agent:uninstall**). Create a custom policy with the action to delete key pairs, set its **Effect** to **Deny**, and assign both this and the **HSS Administrator** policies to the group the user belongs to. Then the user can perform all operations on HSS except uninstalling it. The following is an example policy that denies agent uninstallation.

   .. code-block::

      {
              "Version": "1.1",
              "Statement": [
                      {
                              "Effect": "Deny",
                              "Action": [
                                      "hss:agent:uninstall"
                              ]
                      },
              ]
      }

-  Multi-action policies

   A custom policy can contain the actions of multiple services that are of the project-level type. The following is a policy with multiple statements:

   .. code-block::

      {
              "Version": "1.1",
              "Statement": [
                      {
                              "Effect": "Allow",
                              "Action": [
                                      "hss:hosts:list"
                              ]
                      },
                     {
                              "Effect": "Allow",
                              "Action": [
                                      "hss:hosts:switchVersion",
                                      "hss:hosts:manualDetect",
                                      "hss:manualDetectStatus:get"
                              ]
                      }
              ]
      }

:original_name: hss_01_0368.html

.. _hss_01_0368:

Creating a Policy Group
=======================

For premium and container editions, you can copy a policy group and customize it as required to meet server security requirements in different application scenarios.

Procedure
---------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **HSS**. The HSS page is displayed.

#. In the navigation tree on the left, choose **Security Operation** > **Policies**. On the displayed page, :ref:`Policy group parameters <hss_01_0368__hss_01_0045_t801bc5e996a743dd8e2bfeb480ff1ca8>` describes the fields.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.

   .. _hss_01_0368__hss_01_0045_t801bc5e996a743dd8e2bfeb480ff1ca8:

   .. table:: **Table 1** Policy group parameters

      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                                        |
      +===================================+====================================================================================================================================================================================+
      | Policy Group                      | Name of a policy group The preset policy group names are as follows:                                                                                                               |
      |                                   |                                                                                                                                                                                    |
      |                                   | -  **tenant_linux_container_default_policy_group**: preset Linux policy of the container edition. You can copy this policy group and create a new one based on it.                 |
      |                                   | -  **tenant_linux_enterprise_default_policy_group** is the default Linux policy of the enterprise edition. This policy group can only be viewed, and cannot be copied or deleted.  |
      |                                   | -  **tenant_windows_enterprise_default_policy_group**: preset Windows policy of the enterprise edition. This policy group can only be viewed, and cannot be copied or deleted.     |
      |                                   | -  **tenant_linux_premium_default_policy_group**: preset Linux policy of the premium edition. You can create a policy group by copying this default group and modify the copy.     |
      |                                   | -  **tenant_windows_premium_default_policy_group**: preset Windows policy of the premium edition. You can create a policy group by copying this default group and modify the copy. |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | ID                                | Unique ID of a policy group                                                                                                                                                        |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Description                       | Description of a policy group                                                                                                                                                      |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Supported Version                 | HSS edition supported by a policy group.                                                                                                                                           |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Associated Servers                | To view details about the servers associated with a policy group, click the number in the **Servers** column of the group.                                                         |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Select a premium or container edition policy group and click **Copy** in the **Operation** column of the policy group.


   .. figure:: /_static/images/en-us_image_0000001816051597.png
      :alt: **Figure 1** Copying a policy group

      **Figure 1** Copying a policy group

#. In the dialog box displayed, enter a policy group name and description, and click **OK**.

   .. note::

      -  The name of a policy group must be unique, or the group will fail to be created.
      -  The policy group name and its description can contain only letters, digits, underscores (_), hyphens (-), and spaces, and cannot start or end with a space.

#. Click **OK**.

   After a policy group is created, you can configure rules for each policy in the policy group. For details, see :ref:`Configuring Policies <hss_01_0044>`.

Follow-up Procedure
-------------------

After creating a policy group and configuring policies, you can apply the new policy group to servers. For details, see :ref:`Deploying a Policy <hss_01_0024>`.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

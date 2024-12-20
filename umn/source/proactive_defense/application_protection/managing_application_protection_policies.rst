:original_name: hss_01_0459.html

.. _hss_01_0459:

Managing Application Protection Policies
========================================

Scenario
--------

Application protection policies can be added, edited, and deleted in the following scenarios:

-  Addition: HSS provides a default policy, which contains all the detection rules for application protection. If you need to customize the policy for a server, you can add a protection policy and customize the detection rules and configurations in the policy.
-  Editing: You can edit a custom protection policy.
-  Deletion: You can delete a custom protection policy that is not associated with any server.

Adding a Protection Policy
--------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. Choose **Prevention**\ **Application Protection** and click **Protection Policies**. For more information, see :ref:`Table 1 <hss_01_0459__table18733134319493>`.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.


   .. figure:: /_static/images/en-us_image_0000001854004617.png
      :alt: **Figure 1** Viewing the protection policies

      **Figure 1** Viewing the protection policies

   .. _hss_01_0459__table18733134319493:

   .. table:: **Table 1** Protection policy parameters

      ================== ======================================
      Parameter          Description
      ================== ======================================
      Policy Name        Protection policy name
      Detection Rule     Detection rules supported by a policy.
      Associated Servers Number of servers bound to a policy.
      ================== ======================================

#. Click **Add Policy**. In the dialog box that is displayed, configure the parameters by referring to :ref:`Table 2 <hss_01_0459__table926712416599>`.


   .. figure:: /_static/images/en-us_image_0000001621154510.png
      :alt: **Figure 2** Adding a protection policy

      **Figure 2** Adding a protection policy

   .. _hss_01_0459__table926712416599:

   .. table:: **Table 2** Application protection policy parameters

      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                        |
      +===================================+====================================================================================================================================================================+
      | Policy Name                       | User-defined policy name                                                                                                                                           |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Enabled                           | Whether to enable a detection rule for the current policy. You can select detection rules to enable them as required.                                              |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Detection Rule ID                 | ID of a detection rule.                                                                                                                                            |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Action                            | Protection action of a detection rule.                                                                                                                             |
      |                                   |                                                                                                                                                                    |
      |                                   | -  **Detect**: Detects objects based on the target rule and reports alarms for detected risk events.                                                               |
      |                                   | -  **Detect and block**: Detects objects based on the target rule, reports alarms for detected risk events, and directly blocks or intercepts detected risk items. |
      |                                   |                                                                                                                                                                    |
      |                                   |    .. important::                                                                                                                                                  |
      |                                   |                                                                                                                                                                    |
      |                                   |       NOTICE:                                                                                                                                                      |
      |                                   |       Blocking or interception may interrupt services. Exercise caution when enabling this function                                                                |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Description                       | Description about the detected object and behavior of the target protection policy.                                                                                |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Click **Configure** in the **Operation** column of a detection rule to modify the rule content. :ref:`Table 3 <hss_01_0459__table33641230134112>` describes the supported detection rules.

   .. _hss_01_0459__table33641230134112:

   .. table:: **Table 3** Detection rules that can be configured only

      +----------------+------------------------------------------------+---------------------------------------------------+
      | Rule           | Description                                    | Example                                           |
      +================+================================================+===================================================+
      | XXE            | User-defined XXE blacklist protocol            | .xml;.dtd;                                        |
      +----------------+------------------------------------------------+---------------------------------------------------+
      | XSS            | User-defined XSS shielding rules               | xml;doctype;xmlns;import;entity                   |
      +----------------+------------------------------------------------+---------------------------------------------------+
      | WebShellUpload | User-defined suffix of files in the blacklist. | .jspx;.jsp;.jar;.phtml;.asp;.php;.ascx;.ashx;.cer |
      +----------------+------------------------------------------------+---------------------------------------------------+
      | FileDirAccess  | User-defined path of files in the blacklist.   | /etc/passwd;/etc/shadow;/etc/gshadow;             |
      +----------------+------------------------------------------------+---------------------------------------------------+

#. Confirm the configured policy and selected detection rules, and click **OK**. You can check whether the rule is added on the **Protection Policy** tab page.

Editing a Protection Policy
---------------------------

#. Log in to the management console and go to the HSS page.

#. Choose **Prevention**\ **Application Protection** and click **Protection Policies**. For more information, see :ref:`Table 4 <hss_01_0459__hss_01_0459_table18733134319493>`.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.


   .. figure:: /_static/images/en-us_image_0000001854004617.png
      :alt: **Figure 3** Viewing the protection policies

      **Figure 3** Viewing the protection policies

   .. _hss_01_0459__hss_01_0459_table18733134319493:

   .. table:: **Table 4** Protection policy parameters

      ================== ======================================
      Parameter          Description
      ================== ======================================
      Policy Name        Protection policy name
      Detection Rule     Detection rules supported by a policy.
      Associated Servers Number of servers bound to a policy.
      ================== ======================================

#. Click **Edit** in the **Operation** column of a policy to configure the policy name, supported detection rules, and rule content.

   .. table:: **Table 5** Application protection policy parameters

      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                        |
      +===================================+====================================================================================================================================================================+
      | Policy Name                       | User-defined policy name                                                                                                                                           |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Enabled                           | Whether to enable a detection rule for the current policy. You can select detection rules to enable them as required.                                              |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Detection Rule ID                 | ID of a detection rule.                                                                                                                                            |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Action                            | Protection action of a detection rule.                                                                                                                             |
      |                                   |                                                                                                                                                                    |
      |                                   | -  **Detect**: Detects objects based on the target rule and reports alarms for detected risk events.                                                               |
      |                                   | -  **Detect and block**: Detects objects based on the target rule, reports alarms for detected risk events, and directly blocks or intercepts detected risk items. |
      |                                   |                                                                                                                                                                    |
      |                                   |    .. important::                                                                                                                                                  |
      |                                   |                                                                                                                                                                    |
      |                                   |       NOTICE:                                                                                                                                                      |
      |                                   |       Blocking or interception may interrupt services. Exercise caution when enabling this function                                                                |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Description                       | Description about the detected object and behavior of the target protection policy.                                                                                |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Confirm the configured rule and selected detection items and click **OK**. You can check whether the target policy is modified on the **Protection Policy** tab page.

Deleting a Policy
-----------------

#. Log in to the management console and go to the HSS page.

#. Choose **Prevention**\ **Application Protection** and click **Protection Policies**. For more information, see :ref:`Table 6 <hss_01_0459__hss_01_0459_table18733134319493_1>`.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.


   .. figure:: /_static/images/en-us_image_0000001854004617.png
      :alt: **Figure 4** Viewing the protection policies

      **Figure 4** Viewing the protection policies

   .. _hss_01_0459__hss_01_0459_table18733134319493_1:

   .. table:: **Table 6** Protection policy parameters

      ================== ======================================
      Parameter          Description
      ================== ======================================
      Policy Name        Protection policy name
      Detection Rule     Detection rules supported by a policy.
      Associated Servers Number of servers bound to a policy.
      ================== ======================================

#. Click **Delete** in the **Operation** column of the target policy. In the dialog box that is displayed, confirm the policy information and click **OK**.

   .. important::

      Only the policies that are not associated with any server can be deleted.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

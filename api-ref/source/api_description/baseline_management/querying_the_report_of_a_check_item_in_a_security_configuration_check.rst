:original_name: ShowCheckRuleDetail.html

.. _ShowCheckRuleDetail:

Querying the Report of a Check Item in a Security Configuration Check
=====================================================================

Function
--------

This API is used to query the report of a check item in a security configuration check.

URI
---

GET /v5/{project_id}/baseline/check-rule/detail

.. table:: **Table 1** Path Parameters

   +-----------------+-----------------+-----------------+-----------------+
   | Parameter       | Mandatory       | Type            | Description     |
   +=================+=================+=================+=================+
   | project_id      | Yes             | String          | Project ID      |
   |                 |                 |                 |                 |
   |                 |                 |                 | Minimum: **20** |
   |                 |                 |                 |                 |
   |                 |                 |                 | Maximum: **64** |
   +-----------------+-----------------+-----------------+-----------------+

.. table:: **Table 2** Query Parameters

   +-----------------------+-----------------+-----------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Parameter             | Mandatory       | Type            | Description                                                                                                                                                                                                                                                                                                                                                                                                                                          |
   +=======================+=================+=================+======================================================================================================================================================================================================================================================================================================================================================================================================================================================+
   | enterprise_project_id | No              | String          | Enterprise project ID. The value **0** indicates the default enterprise project. To query all enterprise projects, set this parameter to **all_granted_eps**.                                                                                                                                                                                                                                                                                        |
   |                       |                 |                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
   |                       |                 |                 | Default: **0**                                                                                                                                                                                                                                                                                                                                                                                                                                       |
   |                       |                 |                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
   |                       |                 |                 | Minimum: **0**                                                                                                                                                                                                                                                                                                                                                                                                                                       |
   |                       |                 |                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
   |                       |                 |                 | Maximum: **64**                                                                                                                                                                                                                                                                                                                                                                                                                                      |
   +-----------------------+-----------------+-----------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | check_name            | Yes             | String          | Name of the configuration check (baseline), for example, SSH, CentOS 7, and Windows.                                                                                                                                                                                                                                                                                                                                                                 |
   |                       |                 |                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
   |                       |                 |                 | Minimum: **0**                                                                                                                                                                                                                                                                                                                                                                                                                                       |
   |                       |                 |                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
   |                       |                 |                 | Maximum: **255**                                                                                                                                                                                                                                                                                                                                                                                                                                     |
   +-----------------------+-----------------+-----------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | check_type            | Yes             | String          | Baseline type. You can obtain the value by calling API /v5/{project_id}/baseline/risk-configs. Note that the values for check_type and check_name are the same for Linux servers. For example, they can both be set to SSH or CentOS 7. For Windows servers, the values for check_type and check_name are different. For example, check_type can be set to Windows Server 2019 R2 or Windows Server 2016 R2, while check_name can be set to Windows. |
   |                       |                 |                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
   |                       |                 |                 | Minimum: **0**                                                                                                                                                                                                                                                                                                                                                                                                                                       |
   |                       |                 |                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
   |                       |                 |                 | Maximum: **255**                                                                                                                                                                                                                                                                                                                                                                                                                                     |
   +-----------------------+-----------------+-----------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | check_rule_id         | Yes             | String          | Check item ID, which can be obtained from the return data of this API: /v5/{project_id}/baseline/risk-config/{check_name}/check-rules                                                                                                                                                                                                                                                                                                                |
   |                       |                 |                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
   |                       |                 |                 | Minimum: **0**                                                                                                                                                                                                                                                                                                                                                                                                                                       |
   |                       |                 |                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
   |                       |                 |                 | Maximum: **255**                                                                                                                                                                                                                                                                                                                                                                                                                                     |
   +-----------------------+-----------------+-----------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | standard              | Yes             | String          | hw_standard: Cloud security practice standard                                                                                                                                                                                                                                                                                                                                                                                                        |
   +-----------------------+-----------------+-----------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | host_id               | No              | String          | Host ID                                                                                                                                                                                                                                                                                                                                                                                                                                              |
   |                       |                 |                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
   |                       |                 |                 | Minimum: **0**                                                                                                                                                                                                                                                                                                                                                                                                                                       |
   |                       |                 |                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
   |                       |                 |                 | Maximum: **64**                                                                                                                                                                                                                                                                                                                                                                                                                                      |
   +-----------------------+-----------------+-----------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Request Parameters
------------------

.. table:: **Table 3** Request header parameters

   +-----------------+-----------------+-----------------+----------------------+
   | Parameter       | Mandatory       | Type            | Description          |
   +=================+=================+=================+======================+
   | X-Auth-Token    | Yes             | String          | User token.          |
   |                 |                 |                 |                      |
   |                 |                 |                 | Minimum: **32**      |
   |                 |                 |                 |                      |
   |                 |                 |                 | Maximum: **2097152** |
   +-----------------+-----------------+-----------------+----------------------+

Response Parameters
-------------------

**Status code: 200**

.. table:: **Table 4** Response body parameters

   +-----------------------+-----------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------+
   | Parameter             | Type                                                                                                                  | Description                                             |
   +=======================+=======================================================================================================================+=========================================================+
   | description           | String                                                                                                                | Description of the current check item (detection rule). |
   |                       |                                                                                                                       |                                                         |
   |                       |                                                                                                                       | Minimum: **0**                                          |
   |                       |                                                                                                                       |                                                         |
   |                       |                                                                                                                       | Maximum: **2048**                                       |
   +-----------------------+-----------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------+
   | reference             | String                                                                                                                | Basis for the check item (rule) setting                 |
   |                       |                                                                                                                       |                                                         |
   |                       |                                                                                                                       | Minimum: **0**                                          |
   |                       |                                                                                                                       |                                                         |
   |                       |                                                                                                                       | Maximum: **255**                                        |
   +-----------------------+-----------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------+
   | audit                 | String                                                                                                                | Audit description of the check item (rule)              |
   |                       |                                                                                                                       |                                                         |
   |                       |                                                                                                                       | Minimum: **0**                                          |
   |                       |                                                                                                                       |                                                         |
   |                       |                                                                                                                       | Maximum: **65534**                                      |
   +-----------------------+-----------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------+
   | remediation           | String                                                                                                                | Modification suggestions for the check item (rule)      |
   |                       |                                                                                                                       |                                                         |
   |                       |                                                                                                                       | Minimum: **0**                                          |
   |                       |                                                                                                                       |                                                         |
   |                       |                                                                                                                       | Maximum: **65534**                                      |
   +-----------------------+-----------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------+
   | check_info_list       | Array of :ref:`CheckRuleCheckCaseResponseInfo <showcheckruledetail__response_checkrulecheckcaseresponseinfo>` objects | Test cases                                              |
   |                       |                                                                                                                       |                                                         |
   |                       |                                                                                                                       | Array Length: **0 - 2147483647**                        |
   +-----------------------+-----------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------+

.. _showcheckruledetail__response_checkrulecheckcaseresponseinfo:

.. table:: **Table 5** CheckRuleCheckCaseResponseInfo

   +-----------------------+-----------------------+-----------------------+
   | Parameter             | Type                  | Description           |
   +=======================+=======================+=======================+
   | check_description     | String                | Test case description |
   |                       |                       |                       |
   |                       |                       | Minimum: **0**        |
   |                       |                       |                       |
   |                       |                       | Maximum: **65534**    |
   +-----------------------+-----------------------+-----------------------+
   | current_value         | String                | Current result        |
   |                       |                       |                       |
   |                       |                       | Minimum: **0**        |
   |                       |                       |                       |
   |                       |                       | Maximum: **65534**    |
   +-----------------------+-----------------------+-----------------------+
   | suggest_value         | String                | Expected result       |
   |                       |                       |                       |
   |                       |                       | Minimum: **0**        |
   |                       |                       |                       |
   |                       |                       | Maximum: **65534**    |
   +-----------------------+-----------------------+-----------------------+

Example Requests
----------------

This API is used to query the report of the configuration check items whose baseline name is SSH, check item ID is 1.12, check standard is cloud security practice standard, and enterprise project ID is xxx.

.. code-block:: text

   GET https://{endpoint}/v5/{project_id}/baseline/check-rule/detail?standard=hw_standard&enterprise_project_id=xxx&check_name=SSH&check_type=SSH&check_rule_id=1.12

Example Responses
-----------------

**Status code: 200**

configuration item check report

.. code-block::

   {
     "audit" : "Run the following commands and verify that ClientAliveInterval is smaller than 300 and ClientAliveCountMax is 3 or less: \n#grep '^ClientAliveInterval' /etc/ssh/sshd_config\nClientAliveInterval 300(default is 0) \n#grep '^ClientAliveCountMax' /etc/ssh/sshd_config\nClientAliveCountMax 0(default is 3)",
     "description" : "The two options ClientAliveInterval and ClientAliveCountMax control the timeout of SSH sessions. The ClientAliveInterval parameter sets a timeout interval in seconds after which if no data has been received from the client, sshd will send a message through the encrypted channel to request a response from the client. The ClientAliveCountMax parameter sets the number of client alive messages which may be sent without sshd receiving any messages back from the client. For example, if the ClientAliveInterval is set to 15s and the ClientAliveCountMax is set to 3, unresponsive SSH clients will be disconnected after approximately 45s.",
     "reference" : "",
     "remediation" : "Edit the /etc/ssh/sshd_config file to set the parameter as follows: \nClientAliveInterval 300 \nClientAliveCountMax 0"
   }

Status Codes
------------

=========== ===============================
Status Code Description
=========== ===============================
200         configuration item check report
=========== ===============================

Error Codes
-----------

See :ref:`Error Codes <errorcode>`.

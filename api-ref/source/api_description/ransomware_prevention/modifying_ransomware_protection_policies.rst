:original_name: UpdateProtectionPolicy.html

.. _UpdateProtectionPolicy:

Modifying Ransomware Protection Policies
========================================

Function
--------

This API is used to modify ransomware protection policies.

URI
---

PUT /v5/{project_id}/ransomware/protection/policy

.. table:: **Table 1** Path Parameters

   +-----------------+-----------------+-----------------+------------------+
   | Parameter       | Mandatory       | Type            | Description      |
   +=================+=================+=================+==================+
   | project_id      | Yes             | String          | Project ID       |
   |                 |                 |                 |                  |
   |                 |                 |                 | Minimum: **1**   |
   |                 |                 |                 |                  |
   |                 |                 |                 | Maximum: **256** |
   +-----------------+-----------------+-----------------+------------------+

.. table:: **Table 2** Query Parameters

   +-----------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Parameter             | Mandatory       | Type            | Description                                                                                                                                                   |
   +=======================+=================+=================+===============================================================================================================================================================+
   | enterprise_project_id | No              | String          | Enterprise project ID. The value **0** indicates the default enterprise project. To query all enterprise projects, set this parameter to **all_granted_eps**. |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Default: **0**                                                                                                                                                |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Minimum: **1**                                                                                                                                                |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Maximum: **256**                                                                                                                                              |
   +-----------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+

Request Parameters
------------------

.. table:: **Table 3** Request header parameters

   +-----------------+-----------------+-----------------+--------------------+
   | Parameter       | Mandatory       | Type            | Description        |
   +=================+=================+=================+====================+
   | X-Auth-Token    | Yes             | String          | User token.        |
   |                 |                 |                 |                    |
   |                 |                 |                 | Minimum: **1**     |
   |                 |                 |                 |                    |
   |                 |                 |                 | Maximum: **32768** |
   +-----------------+-----------------+-----------------+--------------------+

.. table:: **Table 4** Request body parameters

   +--------------------------+-----------------+------------------+----------------------------------------------------------------------------------------------------------------------------+
   | Parameter                | Mandatory       | Type             | Description                                                                                                                |
   +==========================+=================+==================+============================================================================================================================+
   | policy_id                | Yes             | String           | Policy ID                                                                                                                  |
   |                          |                 |                  |                                                                                                                            |
   |                          |                 |                  | Minimum: **0**                                                                                                             |
   |                          |                 |                  |                                                                                                                            |
   |                          |                 |                  | Maximum: **128**                                                                                                           |
   +--------------------------+-----------------+------------------+----------------------------------------------------------------------------------------------------------------------------+
   | policy_name              | Yes             | String           | Policy name                                                                                                                |
   |                          |                 |                  |                                                                                                                            |
   |                          |                 |                  | Minimum: **0**                                                                                                             |
   |                          |                 |                  |                                                                                                                            |
   |                          |                 |                  | Maximum: **128**                                                                                                           |
   +--------------------------+-----------------+------------------+----------------------------------------------------------------------------------------------------------------------------+
   | protection_mode          | Yes             | String           | Action. Its value can be:                                                                                                  |
   |                          |                 |                  |                                                                                                                            |
   |                          |                 |                  | -  alarm_and_isolation: Report an alarm and isolate.                                                                       |
   |                          |                 |                  |                                                                                                                            |
   |                          |                 |                  | -  alarm_only: Only report alarms.                                                                                         |
   +--------------------------+-----------------+------------------+----------------------------------------------------------------------------------------------------------------------------+
   | bait_protection_status   | Yes             | String           | Whether to enable honeypot protection. By default, the protection is enabled. Its value can be:                            |
   |                          |                 |                  |                                                                                                                            |
   |                          |                 |                  | -  opened                                                                                                                  |
   |                          |                 |                  |                                                                                                                            |
   |                          |                 |                  | -  closed                                                                                                                  |
   +--------------------------+-----------------+------------------+----------------------------------------------------------------------------------------------------------------------------+
   | protection_directory     | Yes             | String           | Protected directory. Separate multiple directories with semicolons (;). You can configure up to 20 directories.            |
   |                          |                 |                  |                                                                                                                            |
   |                          |                 |                  | Minimum: **1**                                                                                                             |
   |                          |                 |                  |                                                                                                                            |
   |                          |                 |                  | Maximum: **128**                                                                                                           |
   +--------------------------+-----------------+------------------+----------------------------------------------------------------------------------------------------------------------------+
   | protection_type          | Yes             | String           | Protected file type, for example, .docx, .txt, and .avi.                                                                   |
   |                          |                 |                  |                                                                                                                            |
   |                          |                 |                  | Minimum: **1**                                                                                                             |
   |                          |                 |                  |                                                                                                                            |
   |                          |                 |                  | Maximum: **128**                                                                                                           |
   +--------------------------+-----------------+------------------+----------------------------------------------------------------------------------------------------------------------------+
   | exclude_directory        | No              | String           | (Optional) Excluded directory. Separate multiple directories with semicolons (;). You can configure up to 20 directories.  |
   |                          |                 |                  |                                                                                                                            |
   |                          |                 |                  | Minimum: **1**                                                                                                             |
   |                          |                 |                  |                                                                                                                            |
   |                          |                 |                  | Maximum: **128**                                                                                                           |
   +--------------------------+-----------------+------------------+----------------------------------------------------------------------------------------------------------------------------+
   | agent_id_list            | No              | Array of strings | Specifies the IDs of agents for which the ransomware protection policy is enabled.                                         |
   |                          |                 |                  |                                                                                                                            |
   |                          |                 |                  | Minimum: **1**                                                                                                             |
   |                          |                 |                  |                                                                                                                            |
   |                          |                 |                  | Maximum: **128**                                                                                                           |
   |                          |                 |                  |                                                                                                                            |
   |                          |                 |                  | Array Length: **0 - 10000**                                                                                                |
   +--------------------------+-----------------+------------------+----------------------------------------------------------------------------------------------------------------------------+
   | operating_system         | Yes             | String           | OSs supported by the policy. The options are as follows:                                                                   |
   |                          |                 |                  |                                                                                                                            |
   |                          |                 |                  | -  Windows                                                                                                                 |
   |                          |                 |                  |                                                                                                                            |
   |                          |                 |                  | -  Linux                                                                                                                   |
   +--------------------------+-----------------+------------------+----------------------------------------------------------------------------------------------------------------------------+
   | runtime_detection_status | No              | String           | Whether to perform runtime checks. The options are as follows. Currently, it can only be disabled. This field is reserved. |
   |                          |                 |                  |                                                                                                                            |
   |                          |                 |                  | -  opened                                                                                                                  |
   |                          |                 |                  |                                                                                                                            |
   |                          |                 |                  | -  closed                                                                                                                  |
   +--------------------------+-----------------+------------------+----------------------------------------------------------------------------------------------------------------------------+

Response Parameters
-------------------

None

Example Requests
----------------

Modify the ransomware protection policy. Set the OS type to Linux, protection policy ID to 0253edfd-30e7-439d-8f3f-17c54c997064, and protection action to alert only.

.. code-block:: text

   PUT https://{endpoint}/v5/{project_id}/ransomware/protection/policy

   {
     "bait_protection_status" : "opened",
     "exclude_directory" : "",
     "operating_system" : "Linux",
     "policy_id" : "0253edfd-30e7-439d-8f3f-17c54c997064",
     "policy_name" : "aaa",
     "protection_mode" : "alarm_only",
     "protection_directory" : "/root",
     "runtime_detection_status" : "closed",
     "agent_id_list" : [ "" ]
   }

Example Responses
-----------------

None

Status Codes
------------

=========== ===========
Status Code Description
=========== ===========
200         success
=========== ===========

Error Codes
-----------

See :ref:`Error Codes <errorcode>`.

:original_name: AssociatePolicyGroup.html

.. _AssociatePolicyGroup:

Applying a Policy Group
=======================

Function
--------

Applying a policy group

URI
---

POST /v5/{project_id}/policy/deploy

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

   +-----------------+-----------------+-----------------+------------------------------------------------+
   | Parameter       | Mandatory       | Type            | Description                                    |
   +=================+=================+=================+================================================+
   | X-Auth-Token    | Yes             | String          | User token.                                    |
   |                 |                 |                 |                                                |
   |                 |                 |                 | Minimum: **1**                                 |
   |                 |                 |                 |                                                |
   |                 |                 |                 | Maximum: **32768**                             |
   +-----------------+-----------------+-----------------+------------------------------------------------+
   | Content-Type    | No              | String          | Default value: application/json; charset=utf-8 |
   |                 |                 |                 |                                                |
   |                 |                 |                 | Minimum: **0**                                 |
   |                 |                 |                 |                                                |
   |                 |                 |                 | Maximum: **128**                               |
   +-----------------+-----------------+-----------------+------------------------------------------------+

.. table:: **Table 4** Request body parameters

   +------------------------+-----------------+------------------+--------------------------------------------------------------------------------------+
   | Parameter              | Mandatory       | Type             | Description                                                                          |
   +========================+=================+==================+======================================================================================+
   | target_policy_group_id | Yes             | String           | ID of the policy group to be deployed                                                |
   |                        |                 |                  |                                                                                      |
   |                        |                 |                  | Minimum: **36**                                                                      |
   |                        |                 |                  |                                                                                      |
   |                        |                 |                  | Maximum: **64**                                                                      |
   +------------------------+-----------------+------------------+--------------------------------------------------------------------------------------+
   | operate_all            | No              | Boolean          | Whether to deploy the policy for all servers.                                        |
   |                        |                 |                  |                                                                                      |
   |                        |                 |                  | -  true: The policy is deployed on all servers. You do not need to set host_id_list. |
   |                        |                 |                  |                                                                                      |
   |                        |                 |                  | -  false: The policy is not deployed on all servers. You need to set host_id_list.   |
   +------------------------+-----------------+------------------+--------------------------------------------------------------------------------------+
   | host_id_list           | No              | Array of strings | IDs of servers where the policy group needs to be deployed                           |
   |                        |                 |                  |                                                                                      |
   |                        |                 |                  | Minimum: **1**                                                                       |
   |                        |                 |                  |                                                                                      |
   |                        |                 |                  | Maximum: **128**                                                                     |
   |                        |                 |                  |                                                                                      |
   |                        |                 |                  | Array Length: **0 - 10000**                                                          |
   +------------------------+-----------------+------------------+--------------------------------------------------------------------------------------+

Response Parameters
-------------------

None

Example Requests
----------------

Deploy a server protection policy. The target server ID is 15462c0e-32c6-4217-a869-bbd131a00ecf, and the target policy ID is f671f7-2677-4705-a320-de1a62bff306.

.. code-block:: text

   POST https://{endpoint}/v5/{project_id}/policy/deploy

   {
     "target_policy_group_id" : "1df671f7-2677-4705-a320-de1a62bff306",
     "host_id_list" : [ "15462c0e-32c6-4217-a869-bbd131a00ecf" ],
     "operate_all" : false
   }

Example Responses
-----------------

None

Status Codes
------------

=========== ========================
Status Code Description
=========== ========================
200         Success
400         Invalid parameter.
401         Authentication failed.
403         Insufficient permission.
404         Resource not found.
500         System error.
=========== ========================

Error Codes
-----------

See :ref:`Error Codes <errorcode>`.

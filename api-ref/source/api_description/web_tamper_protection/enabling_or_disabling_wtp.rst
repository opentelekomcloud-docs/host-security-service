:original_name: SetWtpProtectionStatusInfo.html

.. _SetWtpProtectionStatusInfo:

Enabling or Disabling WTP
=========================

Function
--------

This API is used to enable or disable WTP.

URI
---

POST /v5/{project_id}/webtamper/static/status

.. table:: **Table 1** Path Parameters

   +-----------------+-----------------+-----------------+-----------------+
   | Parameter       | Mandatory       | Type            | Description     |
   +=================+=================+=================+=================+
   | project_id      | Yes             | String          | Project ID      |
   |                 |                 |                 |                 |
   |                 |                 |                 | Minimum: **0**  |
   |                 |                 |                 |                 |
   |                 |                 |                 | Maximum: **64** |
   +-----------------+-----------------+-----------------+-----------------+

.. table:: **Table 2** Query Parameters

   +-----------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Parameter             | Mandatory       | Type            | Description                                                                                                                                                   |
   +=======================+=================+=================+===============================================================================================================================================================+
   | enterprise_project_id | No              | String          | Enterprise project ID. The value **0** indicates the default enterprise project. To query all enterprise projects, set this parameter to **all_granted_eps**. |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Default: **0**                                                                                                                                                |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Minimum: **0**                                                                                                                                                |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Maximum: **64**                                                                                                                                               |
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

   +-----------------+-----------------+------------------+---------------------------------------------------------------------------------------------------------+
   | Parameter       | Mandatory       | Type             | Description                                                                                             |
   +=================+=================+==================+=========================================================================================================+
   | status          | Yes             | Boolean          | Whether to enable the function. **true**: The function is enabled. **false**: The function is disabled. |
   +-----------------+-----------------+------------------+---------------------------------------------------------------------------------------------------------+
   | host_id_list    | Yes             | Array of strings | The value in the array is server ID and the server ID cannot be empty.                                  |
   |                 |                 |                  |                                                                                                         |
   |                 |                 |                  | Minimum: **0**                                                                                          |
   |                 |                 |                  |                                                                                                         |
   |                 |                 |                  | Maximum: **128**                                                                                        |
   |                 |                 |                  |                                                                                                         |
   |                 |                 |                  | Array Length: **1 - 20000**                                                                             |
   +-----------------+-----------------+------------------+---------------------------------------------------------------------------------------------------------+
   | resource_id     | No              | String           | Resource ID                                                                                             |
   |                 |                 |                  |                                                                                                         |
   |                 |                 |                  | Minimum: **0**                                                                                          |
   |                 |                 |                  |                                                                                                         |
   |                 |                 |                  | Maximum: **64**                                                                                         |
   +-----------------+-----------------+------------------+---------------------------------------------------------------------------------------------------------+

Response Parameters
-------------------

None

Example Requests
----------------

Enable WTP, set the target server IDs to a and b, and pay for the yearly/monthly billing mode.

.. code-block:: text

   POST https://{endpoint}/v5/{project_id}/webtamper/static/status

   {
     "status" : true,
     "host_id_list" : [ "a", "b" ],
     "resource_id" : "aaxxx",
     "charging_mode" : "on_demand"
   }

Example Responses
-----------------

None

Status Codes
------------

=========== ===================
Status Code Description
=========== ===================
200         successful response
=========== ===================

Error Codes
-----------

See :ref:`Error Codes <errorcode>`.

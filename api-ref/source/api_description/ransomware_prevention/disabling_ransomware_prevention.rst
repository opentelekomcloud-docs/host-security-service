:original_name: StopProtection.html

.. _StopProtection:

Disabling Ransomware Prevention
===============================

Function
--------

This API is used to disable ransomware prevention.

URI
---

POST /v5/{project_id}/ransomware/protection/close

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

   +-----------------------+-----------------+------------------+-----------------------------------------------------------------------------------------------------------------------------------------+
   | Parameter             | Mandatory       | Type             | Description                                                                                                                             |
   +=======================+=================+==================+=========================================================================================================================================+
   | host_id_list          | Yes             | Array of strings | IDs of servers where ransomware protection needs to be disabled                                                                         |
   |                       |                 |                  |                                                                                                                                         |
   |                       |                 |                  | Minimum: **0**                                                                                                                          |
   |                       |                 |                  |                                                                                                                                         |
   |                       |                 |                  | Maximum: **64**                                                                                                                         |
   |                       |                 |                  |                                                                                                                                         |
   |                       |                 |                  | Array Length: **0 - 20**                                                                                                                |
   +-----------------------+-----------------+------------------+-----------------------------------------------------------------------------------------------------------------------------------------+
   | agent_id_list         | Yes             | Array of strings | IDs of agents where ransomware prevention needs to be disabled                                                                          |
   |                       |                 |                  |                                                                                                                                         |
   |                       |                 |                  | Minimum: **0**                                                                                                                          |
   |                       |                 |                  |                                                                                                                                         |
   |                       |                 |                  | Maximum: **64**                                                                                                                         |
   |                       |                 |                  |                                                                                                                                         |
   |                       |                 |                  | Array Length: **0 - 20**                                                                                                                |
   +-----------------------+-----------------+------------------+-----------------------------------------------------------------------------------------------------------------------------------------+
   | close_protection_type | Yes             | String           | Type of disabled protection. The options are as follows:                                                                                |
   |                       |                 |                  |                                                                                                                                         |
   |                       |                 |                  | -  close_anti: Disable ransomware protection. Currently, backup protection cannot be disabled. Go to the CBR service to unbind a vault. |
   +-----------------------+-----------------+------------------+-----------------------------------------------------------------------------------------------------------------------------------------+

Response Parameters
-------------------

None

Example Requests
----------------

Disable ransomware protection for the server. The target server ID is 71a15ecc-049f-4cca-bd28-5e90aca1817f, and the agent ID of the target server is c9bed5397db449ebdfba15e85fcfc36accee954daf5cab0528bab59bd8.

.. code-block:: text

   POST https://{endpoint}/v5/{project_id}/ransomware/protection/close

   {
     "close_protection_type" : "close_anti",
     "host_id_list" : [ "71a15ecc-049f-4cca-bd28-5e90aca1817f" ],
     "agent_id_list" : [ "c9bed5397db449ebdfba15e85fcfc36accee954daf5cab0528bab59bd8" ]
   }

Example Responses
-----------------

None

Status Codes
------------

=========== ===============================
Status Code Description
=========== ===============================
200         Ransomware protection disabled.
=========== ===============================

Error Codes
-----------

See :ref:`Error Codes <errorcode>`.

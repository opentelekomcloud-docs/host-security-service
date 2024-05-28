:original_name: ChangeHostsGroup.html

.. _ChangeHostsGroup:

Editing a Server Group
======================

Function
--------

This API is used to edit a server group.

URI
---

PUT /v5/{project_id}/host-management/groups

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

   ============ ========= ================ =================
   Parameter    Mandatory Type             Description
   ============ ========= ================ =================
   group_name   No        String           Server group name
   group_id     Yes       String           Server group ID
   host_id_list No        Array of strings Server ID list
   ============ ========= ================ =================

Response Parameters
-------------------

None

Example Requests
----------------

Edit the server group named test. The server group ID is eca40dbe-27f7-4229-8f9d-a58213129fdc. The IDs of the servers in the server group are 15dac7fe-d81b-43bc-a4a7-4710fe673972 and 21303c5b-36ad-4510-a1b0-cb4ac4c2875c.

.. code-block:: text

   PUT https://{endpoint}/v5/{project_id}/host-management/groups

   {
     "group_id" : "eca40dbe-27f7-4229-8f9d-a58213129fdc",
     "group_name" : "test",
     "host_id_list" : [ "15dac7fe-d81b-43bc-a4a7-4710fe673972", "21303c5b-36ad-4510-a1b0-cb4ac4c2875c" ]
   }

Example Responses
-----------------

None

Status Codes
------------

=========== ========================
Status Code Description
=========== ========================
200         success
400         Invalid parameter.
401         Authentication failed.
403         Insufficient permission.
404         Resource not found.
500         System error.
=========== ========================

Error Codes
-----------

See :ref:`Error Codes <errorcode>`.

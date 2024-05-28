:original_name: AddHostsGroup.html

.. _AddHostsGroup:

Creating a Server Group
=======================

Function
--------

This API is used to create a server group.

URI
---

POST /v5/{project_id}/host-management/groups

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

   +-----------------+-----------------+------------------+-----------------------------+
   | Parameter       | Mandatory       | Type             | Description                 |
   +=================+=================+==================+=============================+
   | group_name      | Yes             | String           | Server group name           |
   |                 |                 |                  |                             |
   |                 |                 |                  | Minimum: **1**              |
   |                 |                 |                  |                             |
   |                 |                 |                  | Maximum: **128**            |
   +-----------------+-----------------+------------------+-----------------------------+
   | host_id_list    | Yes             | Array of strings | Server ID list              |
   |                 |                 |                  |                             |
   |                 |                 |                  | Minimum: **1**              |
   |                 |                 |                  |                             |
   |                 |                 |                  | Maximum: **128**            |
   |                 |                 |                  |                             |
   |                 |                 |                  | Array Length: **1 - 10000** |
   +-----------------+-----------------+------------------+-----------------------------+

Response Parameters
-------------------

None

Example Requests
----------------

Create a server group named test. The ID of the server in the server group is 15dac7fe-d81b-43bc-a4a7-4710fe673972.

.. code-block:: text

   POST https://{endpoint}/v5/{project_id}/host-management/groups

   {
     "group_name" : "test",
     "host_id_list" : [ "15dac7fe-d81b-43bc-a4a7-4710fe673972" ]
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

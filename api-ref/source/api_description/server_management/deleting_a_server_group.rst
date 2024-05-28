:original_name: DeleteHostsGroup.html

.. _DeleteHostsGroup:

Deleting a Server Group
=======================

Function
--------

This API is used to delete a server group.

URI
---

DELETE /v5/{project_id}/host-management/groups

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
   | group_id              | Yes             | String          | Server group ID                                                                                                                                               |
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

Response Parameters
-------------------

None

Example Requests
----------------

Delete the server group whose ID is 34fcf861-402b-45c6-9b6a-13087791aae3.

.. code-block:: text

   DELETE https://{endpoint}/v5/{project_id}/host-management/groups

   {
     "group_id" : "34fcf861-402b-45c6-9b6a-13087791aae3"
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

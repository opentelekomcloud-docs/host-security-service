:original_name: DeleteResourceInstanceTag.html

.. _DeleteResourceInstanceTag:

Deleting a Resource Tag
=======================

Function
--------

This API is used to delete a tag from a resource.

URI
---

DELETE /v5/{project_id}/{resource_type}/{resource_id}/tags/{key}

.. table:: **Table 1** Path Parameters

   +-----------------+-----------------+-----------------+--------------------------------------------------------------------------------------+
   | Parameter       | Mandatory       | Type            | Description                                                                          |
   +=================+=================+=================+======================================================================================+
   | project_id      | Yes             | String          | Project ID                                                                           |
   |                 |                 |                 |                                                                                      |
   |                 |                 |                 | Minimum: **1**                                                                       |
   |                 |                 |                 |                                                                                      |
   |                 |                 |                 | Maximum: **256**                                                                     |
   +-----------------+-----------------+-----------------+--------------------------------------------------------------------------------------+
   | resource_type   | Yes             | String          | Resource type defined by TMS. When HSS calls the API, the resource type is HSS.      |
   |                 |                 |                 |                                                                                      |
   |                 |                 |                 | Minimum: **1**                                                                       |
   |                 |                 |                 |                                                                                      |
   |                 |                 |                 | Maximum: **64**                                                                      |
   +-----------------+-----------------+-----------------+--------------------------------------------------------------------------------------+
   | resource_id     | Yes             | String          | Resource ID defined by TMS. When HSS calls the API, the resource ID is the quota ID. |
   |                 |                 |                 |                                                                                      |
   |                 |                 |                 | Minimum: **0**                                                                       |
   |                 |                 |                 |                                                                                      |
   |                 |                 |                 | Maximum: **128**                                                                     |
   +-----------------+-----------------+-----------------+--------------------------------------------------------------------------------------+
   | key             | Yes             | String          | Key to be deleted                                                                    |
   |                 |                 |                 |                                                                                      |
   |                 |                 |                 | Minimum: **1**                                                                       |
   |                 |                 |                 |                                                                                      |
   |                 |                 |                 | Maximum: **256**                                                                     |
   +-----------------+-----------------+-----------------+--------------------------------------------------------------------------------------+

Request Parameters
------------------

.. table:: **Table 2** Request header parameters

   +-----------------+-----------------+-----------------+------------------+
   | Parameter       | Mandatory       | Type            | Description      |
   +=================+=================+=================+==================+
   | X-Auth-Token    | Yes             | String          | User token.      |
   |                 |                 |                 |                  |
   |                 |                 |                 | Minimum: **32**  |
   |                 |                 |                 |                  |
   |                 |                 |                 | Maximum: **512** |
   +-----------------+-----------------+-----------------+------------------+

Response Parameters
-------------------

None

Example Requests
----------------

Delete the tag whose key is abc, project_id is 94b5266c14ce489fa6549817f032dc61, resource_type is hss, and resource_id is 2acc46ee-34c2-40c2-8060-dc652e6c672a.

.. code-block:: text

   DELETE https://{endpoint}/v5/94b5266c14ce489fa6549817f032dc61/hss/2acc46ee-34c2-40c2-8060-dc652e6c672a/tags/abc

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
404         Resources not found.
500         System error.
=========== ========================

Error Codes
-----------

See :ref:`Error Codes <errorcode>`.

:original_name: BatchCreateTags.html

.. _BatchCreateTags:

Creating Tags in Batches
========================

Function
--------

This API is used to create tags in batches.

URI
---

POST /v5/{project_id}/{resource_type}/{resource_id}/tags/create

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

Request Parameters
------------------

.. table:: **Table 2** Request header parameters

   +-----------------+-----------------+-----------------+------------------------------------------------+
   | Parameter       | Mandatory       | Type            | Description                                    |
   +=================+=================+=================+================================================+
   | X-Auth-Token    | Yes             | String          | User token.                                    |
   |                 |                 |                 |                                                |
   |                 |                 |                 | Minimum: **32**                                |
   |                 |                 |                 |                                                |
   |                 |                 |                 | Maximum: **512**                               |
   +-----------------+-----------------+-----------------+------------------------------------------------+
   | Content-Type    | No              | String          | Default value: application/json; charset=utf-8 |
   |                 |                 |                 |                                                |
   |                 |                 |                 | Minimum: **0**                                 |
   |                 |                 |                 |                                                |
   |                 |                 |                 | Maximum: **128**                               |
   +-----------------+-----------------+-----------------+------------------------------------------------+

.. table:: **Table 3** Request body parameters

   +-----------------+-----------------+------------------------------------------------------------------------------------+----------------------------+
   | Parameter       | Mandatory       | Type                                                                               | Description                |
   +=================+=================+====================================================================================+============================+
   | tags            | Yes             | Array of :ref:`ResourceTagInfo <batchcreatetags__request_resourcetaginfo>` objects | Tag List                   |
   |                 |                 |                                                                                    |                            |
   |                 |                 |                                                                                    | Array Length: **0 - 1024** |
   +-----------------+-----------------+------------------------------------------------------------------------------------+----------------------------+

.. _batchcreatetags__request_resourcetaginfo:

.. table:: **Table 4** ResourceTagInfo

   +-----------------+-----------------+-----------------+---------------------------------------------------------------------------------+
   | Parameter       | Mandatory       | Type            | Description                                                                     |
   +=================+=================+=================+=================================================================================+
   | key             | Yes             | String          | Key. It can contain up to 128 Unicode characters. The key cannot be left blank. |
   |                 |                 |                 |                                                                                 |
   |                 |                 |                 | Minimum: **1**                                                                  |
   |                 |                 |                 |                                                                                 |
   |                 |                 |                 | Maximum: **128**                                                                |
   +-----------------+-----------------+-----------------+---------------------------------------------------------------------------------+
   | value           | Yes             | String          | Value.                                                                          |
   |                 |                 |                 |                                                                                 |
   |                 |                 |                 | Minimum: **1**                                                                  |
   |                 |                 |                 |                                                                                 |
   |                 |                 |                 | Maximum: **128**                                                                |
   +-----------------+-----------------+-----------------+---------------------------------------------------------------------------------+

Response Parameters
-------------------

None

Example Requests
----------------

Create a tag key TESTKEY20220831190155 (the tag value is 2) and a tag key test (the tag value is hss).

.. code-block:: text

   POST https://{endpoint}/v5/05e1e8b7ba8010dd2f80c01070a8d4cd/hss/fbaa9aca-2b5f-11ee-8c64-fa163e139e02/tags/create

   {
     "tags" : [ {
       "key" : "TESTKEY20220831190155",
       "value" : "2"
     }, {
       "key" : "test",
       "value" : "hss"
     } ]
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
404         Resources not found.
500         System error.
=========== ========================

Error Codes
-----------

See :ref:`Error Codes <errorcode>`.

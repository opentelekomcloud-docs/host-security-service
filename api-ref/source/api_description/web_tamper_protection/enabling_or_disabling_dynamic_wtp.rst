:original_name: SetRaspSwitch.html

.. _SetRaspSwitch:

Enabling or Disabling Dynamic WTP
=================================

Function
--------

This API is used to enable or disable dynamic WTP.

URI
---

POST /v5/{project_id}/webtamper/rasp/status

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

   +-----------------+-----------------+------------------+-----------------------------+
   | Parameter       | Mandatory       | Type             | Description                 |
   +=================+=================+==================+=============================+
   | host_id_list    | No              | Array of strings | HostId list                 |
   |                 |                 |                  |                             |
   |                 |                 |                  | Minimum: **0**              |
   |                 |                 |                  |                             |
   |                 |                 |                  | Maximum: **128**            |
   |                 |                 |                  |                             |
   |                 |                 |                  | Array Length: **0 - 20000** |
   +-----------------+-----------------+------------------+-----------------------------+
   | status          | No              | Boolean          | Dynamic WTP status          |
   +-----------------+-----------------+------------------+-----------------------------+

Response Parameters
-------------------

None

Example Requests
----------------

Enable dynamic WTP for servers a and b.

.. code-block:: text

   POST https://{endpoint}/v5/{project_id}/webtamper/rasp/status

   {
     "host_id_list" : [ "a", "b" ],
     "status" : true
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

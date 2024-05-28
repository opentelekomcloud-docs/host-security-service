:original_name: ListHostGroups.html

.. _ListHostGroups:

Querying Server Groups
======================

Function
--------

This API is used to query server groups.

URI
---

GET /v5/{project_id}/host-management/groups

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
   | offset                | No              | Integer         | Offset, which specifies the start position of the record to be returned.                                                                                      |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Minimum: **0**                                                                                                                                                |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Maximum: **2000000**                                                                                                                                          |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Default: **0**                                                                                                                                                |
   +-----------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | limit                 | No              | Integer         | Number of records displayed on each page.                                                                                                                     |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Minimum: **10**                                                                                                                                               |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Maximum: **200**                                                                                                                                              |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Default: **10**                                                                                                                                               |
   +-----------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | group_name            | No              | String          | Server group name                                                                                                                                             |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Minimum: **1**                                                                                                                                                |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Maximum: **64**                                                                                                                                               |
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

**Status code: 200**

.. table:: **Table 4** Response body parameters

   +-----------------------+--------------------------------------------------------------------------------+---------------------------+
   | Parameter             | Type                                                                           | Description               |
   +=======================+================================================================================+===========================+
   | total_num             | Integer                                                                        | Total number              |
   +-----------------------+--------------------------------------------------------------------------------+---------------------------+
   | data_list             | Array of :ref:`HostGroupItem <listhostgroups__response_hostgroupitem>` objects | Server group list         |
   |                       |                                                                                |                           |
   |                       |                                                                                | Array Length: **0 - 100** |
   +-----------------------+--------------------------------------------------------------------------------+---------------------------+

.. _listhostgroups__response_hostgroupitem:

.. table:: **Table 5** HostGroupItem

   ================== ================ =============================
   Parameter          Type             Description
   ================== ================ =============================
   group_id           String           Server group ID
   group_name         String           Server group name
   host_num           Integer          Number of associated servers
   risk_host_num      Integer          Number of unsafe servers
   unprotect_host_num Integer          Number of unprotected servers
   host_id_list       Array of strings Server ID list
   ================== ================ =============================

Example Requests
----------------

Query the server group whose name is test.

.. code-block:: text

   GET https://{endpoint}/v5/{project_id}/host-management/groups?offset=0&limit=200&enterprise_project_id=all_granted_eps&&group_name=test

Example Responses
-----------------

**Status code: 200**

Server group list

.. code-block::

   {
     "data_list" : [ {
       "group_id" : "36e59701-e2e7-4d56-b229-0db3bcf4e6e8",
       "group_name" : "test",
       "host_id_list" : [ "71a15ecc-049f-4cca-bd28-5e90aca1817f" ],
       "host_num" : 1,
       "risk_host_num" : 1,
       "unprotect_host_num" : 0
     } ],
     "total_num" : 1
   }

Status Codes
------------

=========== =================
Status Code Description
=========== =================
200         Server group list
=========== =================

Error Codes
-----------

See :ref:`Error Codes <errorcode>`.

:original_name: ListUserStatistics.html

.. _ListUserStatistics:

Asset Fingerprint - Account Information
=======================================

Function
--------

This API is used to check account information in asset fingerprints.

URI
---

GET /v5/{project_id}/asset/user/statistics

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

   +-----------------------+-----------------+-----------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Parameter             | Mandatory       | Type            | Description                                                                                                                                                          |
   +=======================+=================+=================+======================================================================================================================================================================+
   | user_name             | No              | String          | Account name. It must comply with the Windows file naming rules. The value can contain letters, digits, underscores (_), and the following special characters: !@.-. |
   |                       |                 |                 |                                                                                                                                                                      |
   |                       |                 |                 | Minimum: **1**                                                                                                                                                       |
   |                       |                 |                 |                                                                                                                                                                      |
   |                       |                 |                 | Maximum: **128**                                                                                                                                                     |
   +-----------------------+-----------------+-----------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | enterprise_project_id | No              | String          | Enterprise project ID. The value **0** indicates the default enterprise project. To query all enterprise projects, set this parameter to **all_granted_eps**.        |
   |                       |                 |                 |                                                                                                                                                                      |
   |                       |                 |                 | Default: **0**                                                                                                                                                       |
   |                       |                 |                 |                                                                                                                                                                      |
   |                       |                 |                 | Minimum: **0**                                                                                                                                                       |
   |                       |                 |                 |                                                                                                                                                                      |
   |                       |                 |                 | Maximum: **128**                                                                                                                                                     |
   +-----------------------+-----------------+-----------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | limit                 | No              | Integer         | Number of records on each page.                                                                                                                                      |
   |                       |                 |                 |                                                                                                                                                                      |
   |                       |                 |                 | Minimum: **10**                                                                                                                                                      |
   |                       |                 |                 |                                                                                                                                                                      |
   |                       |                 |                 | Maximum: **200**                                                                                                                                                     |
   |                       |                 |                 |                                                                                                                                                                      |
   |                       |                 |                 | Default: **10**                                                                                                                                                      |
   +-----------------------+-----------------+-----------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | offset                | No              | Integer         | Offset, which specifies the start position of the record to be returned.                                                                                             |
   |                       |                 |                 |                                                                                                                                                                      |
   |                       |                 |                 | Minimum: **0**                                                                                                                                                       |
   |                       |                 |                 |                                                                                                                                                                      |
   |                       |                 |                 | Maximum: **2000000**                                                                                                                                                 |
   |                       |                 |                 |                                                                                                                                                                      |
   |                       |                 |                 | Default: **0**                                                                                                                                                       |
   +-----------------------+-----------------+-----------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Request Parameters
------------------

.. table:: **Table 3** Request header parameters

   +-----------------+-----------------+-----------------+-------------------+
   | Parameter       | Mandatory       | Type            | Description       |
   +=================+=================+=================+===================+
   | X-Auth-Token    | Yes             | String          | User token.       |
   |                 |                 |                 |                   |
   |                 |                 |                 | Minimum: **32**   |
   |                 |                 |                 |                   |
   |                 |                 |                 | Maximum: **4096** |
   +-----------------+-----------------+-----------------+-------------------+

Response Parameters
-------------------

**Status code: 200**

.. table:: **Table 4** Response body parameters

   +-----------------------+--------------------------------------------------------------------------------------------------------------------+-----------------------------+
   | Parameter             | Type                                                                                                               | Description                 |
   +=======================+====================================================================================================================+=============================+
   | total_num             | Integer                                                                                                            | Total number of accounts    |
   |                       |                                                                                                                    |                             |
   |                       |                                                                                                                    | Minimum: **0**              |
   |                       |                                                                                                                    |                             |
   |                       |                                                                                                                    | Maximum: **10000**          |
   +-----------------------+--------------------------------------------------------------------------------------------------------------------+-----------------------------+
   | data_list             | Array of :ref:`UserStatisticInfoResponseInfo <listuserstatistics__response_userstatisticinforesponseinfo>` objects | Account statistics list     |
   |                       |                                                                                                                    |                             |
   |                       |                                                                                                                    | Array Length: **0 - 10000** |
   +-----------------------+--------------------------------------------------------------------------------------------------------------------+-----------------------------+

.. _listuserstatistics__response_userstatisticinforesponseinfo:

.. table:: **Table 5** UserStatisticInfoResponseInfo

   +-----------------------+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Parameter             | Type                  | Description                                                                                                                                                          |
   +=======================+=======================+======================================================================================================================================================================+
   | user_name             | String                | Account name. It must comply with the Windows file naming rules. The value can contain letters, digits, underscores (_), and the following special characters: !@.-. |
   |                       |                       |                                                                                                                                                                      |
   |                       |                       | Minimum: **1**                                                                                                                                                       |
   |                       |                       |                                                                                                                                                                      |
   |                       |                       | Maximum: **128**                                                                                                                                                     |
   +-----------------------+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | num                   | Integer               | Number of servers of the account                                                                                                                                     |
   |                       |                       |                                                                                                                                                                      |
   |                       |                       | Minimum: **0**                                                                                                                                                       |
   |                       |                       |                                                                                                                                                                      |
   |                       |                       | Maximum: **10000**                                                                                                                                                   |
   +-----------------------+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Example Requests
----------------

The first 10 accounts are queried by default.

.. code-block:: text

   GET https://{endpoint}/v5/{project_id}/asset/user/statistics

Example Responses
-----------------

**Status code: 200**

Number of servers having the account

.. code-block::

   {
     "total_num" : 1,
     "data_list" : [ {
       "user_name" : "bin",
       "num" : 5
     } ]
   }

Status Codes
------------

=========== ====================================
Status Code Description
=========== ====================================
200         Number of servers having the account
=========== ====================================

Error Codes
-----------

See :ref:`Error Codes <errorcode>`.

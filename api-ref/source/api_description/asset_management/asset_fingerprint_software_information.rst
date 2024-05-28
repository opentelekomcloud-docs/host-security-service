:original_name: ListAppStatistics.html

.. _ListAppStatistics:

Asset Fingerprint - Software Information
========================================

Function
--------

This API is used to check software information in asset fingerprints.

URI
---

GET /v5/{project_id}/asset/app/statistics

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
   | app_name              | No              | String          | Software name                                                                                                                                                 |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Minimum: **1**                                                                                                                                                |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Maximum: **256**                                                                                                                                              |
   +-----------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | enterprise_project_id | No              | String          | Enterprise project ID. The value **0** indicates the default enterprise project. To query all enterprise projects, set this parameter to **all_granted_eps**. |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Default: **0**                                                                                                                                                |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Minimum: **1**                                                                                                                                                |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Maximum: **256**                                                                                                                                              |
   +-----------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | limit                 | No              | Integer         | Number of records on each page.                                                                                                                               |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Minimum: **10**                                                                                                                                               |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Maximum: **100**                                                                                                                                              |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Default: **10**                                                                                                                                               |
   +-----------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | offset                | No              | Integer         | Offset, which specifies the start position of the record to be returned.                                                                                      |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Minimum: **0**                                                                                                                                                |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Maximum: **10000**                                                                                                                                            |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Default: **0**                                                                                                                                                |
   +-----------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | category              | No              | String          | Type. The default value is host. The options are as follows:                                                                                                  |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | -  host                                                                                                                                                       |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | -  container                                                                                                                                                  |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Minimum: **0**                                                                                                                                                |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Maximum: **64**                                                                                                                                               |
   +-----------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+

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

   +-----------------------+---------------------------------------------------------------------------------------------------------+------------------------------------+
   | Parameter             | Type                                                                                                    | Description                        |
   +=======================+=========================================================================================================+====================================+
   | total_num             | Integer                                                                                                 | Total number of process statistics |
   |                       |                                                                                                         |                                    |
   |                       |                                                                                                         | Minimum: **0**                     |
   |                       |                                                                                                         |                                    |
   |                       |                                                                                                         | Maximum: **10000**                 |
   +-----------------------+---------------------------------------------------------------------------------------------------------+------------------------------------+
   | data_list             | Array of :ref:`AppStatisticResponseInfo <listappstatistics__response_appstatisticresponseinfo>` objects | Process statistics list            |
   |                       |                                                                                                         |                                    |
   |                       |                                                                                                         | Array Length: **0 - 10000**        |
   +-----------------------+---------------------------------------------------------------------------------------------------------+------------------------------------+

.. _listappstatistics__response_appstatisticresponseinfo:

.. table:: **Table 5** AppStatisticResponseInfo

   +-----------------------+-----------------------+-----------------------+
   | Parameter             | Type                  | Description           |
   +=======================+=======================+=======================+
   | app_name              | String                | Software name         |
   |                       |                       |                       |
   |                       |                       | Minimum: **1**        |
   |                       |                       |                       |
   |                       |                       | Maximum: **128**      |
   +-----------------------+-----------------------+-----------------------+
   | num                   | Integer               | Number of processes   |
   |                       |                       |                       |
   |                       |                       | Minimum: **0**        |
   |                       |                       |                       |
   |                       |                       | Maximum: **100000**   |
   +-----------------------+-----------------------+-----------------------+

Example Requests
----------------

The first 10 software lists whose type is host are queried by default.

.. code-block:: text

   GET https://{endpoint}/v5/{project_id}/asset/app/statistics?category=host

Example Responses
-----------------

**Status code: 200**

Number of servers having the software

.. code-block::

   {
     "total_num" : 1,
     "data_list" : [ {
       "app_name" : "kernel",
       "num" : 13
     } ]
   }

Status Codes
------------

=========== =====================================
Status Code Description
=========== =====================================
200         Number of servers having the software
=========== =====================================

Error Codes
-----------

See :ref:`Error Codes <errorcode>`.

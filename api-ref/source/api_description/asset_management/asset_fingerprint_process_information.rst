:original_name: ListProcessStatistics.html

.. _ListProcessStatistics:

Asset Fingerprint - Process Information
=======================================

Function
--------

This API is used to check process information in asset fingerprints.

URI
---

GET /v5/{project_id}/asset/process/statistics

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
   | path                  | No              | String          | Executable process path                                                                                                                                       |
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

   +-----------------------+---------------------------------------------------------------------------------------------------------------------+------------------------------------+
   | Parameter             | Type                                                                                                                | Description                        |
   +=======================+=====================================================================================================================+====================================+
   | total_num             | Integer                                                                                                             | Total number of process statistics |
   |                       |                                                                                                                     |                                    |
   |                       |                                                                                                                     | Minimum: **0**                     |
   |                       |                                                                                                                     |                                    |
   |                       |                                                                                                                     | Maximum: **10000**                 |
   +-----------------------+---------------------------------------------------------------------------------------------------------------------+------------------------------------+
   | data_list             | Array of :ref:`ProcessStatisticResponseInfo <listprocessstatistics__response_processstatisticresponseinfo>` objects | Process statistics list            |
   |                       |                                                                                                                     |                                    |
   |                       |                                                                                                                     | Array Length: **0 - 10000**        |
   +-----------------------+---------------------------------------------------------------------------------------------------------------------+------------------------------------+

.. _listprocessstatistics__response_processstatisticresponseinfo:

.. table:: **Table 5** ProcessStatisticResponseInfo

   +-----------------------+-----------------------+----------------------------------------------+
   | Parameter             | Type                  | Description                                  |
   +=======================+=======================+==============================================+
   | path                  | String                | Path of the executable files for the process |
   |                       |                       |                                              |
   |                       |                       | Minimum: **1**                               |
   |                       |                       |                                              |
   |                       |                       | Maximum: **256**                             |
   +-----------------------+-----------------------+----------------------------------------------+
   | num                   | Integer               | Number of processes                          |
   |                       |                       |                                              |
   |                       |                       | Minimum: **0**                               |
   |                       |                       |                                              |
   |                       |                       | Maximum: **100000**                          |
   +-----------------------+-----------------------+----------------------------------------------+

Example Requests
----------------

The first 10 processes whose type is host are queried by default.

.. code-block:: text

   GET https://{endpoint}/v5/{project_id}/asset/process/statistics?category=host

Example Responses
-----------------

**Status code: 200**

Number of servers having the process

.. code-block::

   {
     "total_num" : 1,
     "data_list" : [ {
       "num" : 13,
       "path" : "/usr/lib/systemd/systemd-journald"
     } ]
   }

Status Codes
------------

=========== ====================================
Status Code Description
=========== ====================================
200         Number of servers having the process
=========== ====================================

Error Codes
-----------

See :ref:`Error Codes <errorcode>`.

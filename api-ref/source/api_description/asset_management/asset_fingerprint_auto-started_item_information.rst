:original_name: ListAutoLaunchStatistics.html

.. _ListAutoLaunchStatistics:

Asset Fingerprint - Auto-Started Item Information
=================================================

Function
--------

This API is used to check auto-started items in asset fingerprints.

URI
---

GET /v5/{project_id}/asset/auto-launch/statistics

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
   | name                  | No              | String          | Auto-started item name                                                                                                                                        |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Minimum: **1**                                                                                                                                                |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Maximum: **256**                                                                                                                                              |
   +-----------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | type                  | No              | String          | Auto-started item type                                                                                                                                        |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | -  0: auto-started service                                                                                                                                    |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | -  1: scheduled task                                                                                                                                          |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | -  2: Preload dynamic library                                                                                                                                 |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | -  3: Run registry key                                                                                                                                        |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | -  4: startup folder                                                                                                                                          |
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

   +-----------------------+--------------------------------------------------------------------------------------------------------------------------------+--------------------------------------+
   | Parameter             | Type                                                                                                                           | Description                          |
   +=======================+================================================================================================================================+======================================+
   | total_num             | Integer                                                                                                                        | Total number of auto-started items   |
   |                       |                                                                                                                                |                                      |
   |                       |                                                                                                                                | Minimum: **0**                       |
   |                       |                                                                                                                                |                                      |
   |                       |                                                                                                                                | Maximum: **10000**                   |
   +-----------------------+--------------------------------------------------------------------------------------------------------------------------------+--------------------------------------+
   | data_list             | Array of :ref:`AutoLaunchStatisticsResponseInfo <listautolaunchstatistics__response_autolaunchstatisticsresponseinfo>` objects | List of auto-started item statistics |
   |                       |                                                                                                                                |                                      |
   |                       |                                                                                                                                | Array Length: **0 - 10000**          |
   +-----------------------+--------------------------------------------------------------------------------------------------------------------------------+--------------------------------------+

.. _listautolaunchstatistics__response_autolaunchstatisticsresponseinfo:

.. table:: **Table 5** AutoLaunchStatisticsResponseInfo

   +-----------------------+-----------------------+--------------------------------------------------------+
   | Parameter             | Type                  | Description                                            |
   +=======================+=======================+========================================================+
   | name                  | String                | Auto-started item name                                 |
   |                       |                       |                                                        |
   |                       |                       | Minimum: **1**                                         |
   |                       |                       |                                                        |
   |                       |                       | Maximum: **256**                                       |
   +-----------------------+-----------------------+--------------------------------------------------------+
   | type                  | String                | Auto-started item type                                 |
   |                       |                       |                                                        |
   |                       |                       | -  0: auto-started service                             |
   |                       |                       |                                                        |
   |                       |                       | -  1: scheduled task                                   |
   |                       |                       |                                                        |
   |                       |                       | -  2: Preload dynamic library                          |
   |                       |                       |                                                        |
   |                       |                       | -  3: Run registry key                                 |
   |                       |                       |                                                        |
   |                       |                       | -  4: startup folder                                   |
   |                       |                       |                                                        |
   |                       |                       | Minimum: **1**                                         |
   |                       |                       |                                                        |
   |                       |                       | Maximum: **11**                                        |
   +-----------------------+-----------------------+--------------------------------------------------------+
   | num                   | Integer               | Indicates the number of servers of auto-started items. |
   |                       |                       |                                                        |
   |                       |                       | Minimum: **0**                                         |
   |                       |                       |                                                        |
   |                       |                       | Maximum: **10000**                                     |
   +-----------------------+-----------------------+--------------------------------------------------------+

Example Requests
----------------

The first 10 auto-startup items are queried by default.

.. code-block:: text

   GET https://{endpoint}/v5/{project_id}/asset/auto-launch/statistics

Example Responses
-----------------

**Status code: 200**

Number of servers having the process

.. code-block::

   {
     "total_num" : 1,
     "data_list" : [ {
       "name" : "S12hostguard",
       "type" : "0",
       "num" : 5
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

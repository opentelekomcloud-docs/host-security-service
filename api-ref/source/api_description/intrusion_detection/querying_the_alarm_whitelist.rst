:original_name: ListAlarmWhiteList.html

.. _ListAlarmWhiteList:

Querying the Alarm Whitelist
============================

Function
--------

This API is used to query the alarm whitelist.

URI
---

GET /v5/{project_id}/event/white-list/alarm

.. table:: **Table 1** Path Parameters

   +-----------------+-----------------+-----------------+-----------------+
   | Parameter       | Mandatory       | Type            | Description     |
   +=================+=================+=================+=================+
   | project_id      | Yes             | String          | Project ID      |
   |                 |                 |                 |                 |
   |                 |                 |                 | Minimum: **20** |
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
   | hash                  | No              | String          | Hash value of the event whitelist description (SHA256 algorithm)                                                                                              |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Minimum: **64**                                                                                                                                               |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Maximum: **64**                                                                                                                                               |
   +-----------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | event_type            | No              | Integer         | Event type. Its value can be:                                                                                                                                 |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | -  1001: malware                                                                                                                                              |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | -  1010 : Rootkit                                                                                                                                             |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | -  1011: ransomware                                                                                                                                           |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 |    -  1015 : Web shell                                                                                                                                        |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 |    -  1017: reverse shell                                                                                                                                     |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 |    -  2001: Common vulnerability exploit                                                                                                                      |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 |    -  2047: redis vulnerability exploit                                                                                                                       |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 |    -  2048: Hadoop vulnerability exploit                                                                                                                      |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 |    -  2049: MySQL vulnerability exploit                                                                                                                       |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 |    -  3002: file privilege escalation                                                                                                                         |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 |    -  3003: process privilege escalation                                                                                                                      |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 |    -  3004: critical file change                                                                                                                              |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 |    -  3005: file/directory change                                                                                                                             |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 |    -  3007: abnormal process behavior                                                                                                                         |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 |    -  3015: high-risk command execution                                                                                                                       |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 |    -  3018: abnormal shell                                                                                                                                    |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 |    -  3027: suspicious crontab task                                                                                                                           |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 |    -  4002: brute-force attack                                                                                                                                |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 |    -  4004: abnormal login                                                                                                                                    |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 |    -  4006: Invalid system account                                                                                                                            |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Minimum: **1000**                                                                                                                                             |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Maximum: **30000**                                                                                                                                            |
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
   |                       |                 |                 | Maximum: **1000**                                                                                                                                             |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Default: **10**                                                                                                                                               |
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

   +-----------------------+--------------------------------------------------------------------------------------------------------------+--------------------------------------+
   | Parameter             | Type                                                                                                         | Description                          |
   +=======================+==============================================================================================================+======================================+
   | total_num             | Integer                                                                                                      | Total number                         |
   +-----------------------+--------------------------------------------------------------------------------------------------------------+--------------------------------------+
   | event_type_list       | Array of integers                                                                                            | Types of events that can be filtered |
   |                       |                                                                                                              |                                      |
   |                       |                                                                                                              | Minimum: **0**                       |
   |                       |                                                                                                              |                                      |
   |                       |                                                                                                              | Maximum: **2147483647**              |
   |                       |                                                                                                              |                                      |
   |                       |                                                                                                              | Array Length: **0 - 30000**          |
   +-----------------------+--------------------------------------------------------------------------------------------------------------+--------------------------------------+
   | data_list             | Array of :ref:`AlarmWhiteListResponseInfo <listalarmwhitelist__response_alarmwhitelistresponseinfo>` objects | Alarm whitelist details              |
   |                       |                                                                                                              |                                      |
   |                       |                                                                                                              | Array Length: **0 - 100**            |
   +-----------------------+--------------------------------------------------------------------------------------------------------------+--------------------------------------+

.. _listalarmwhitelist__response_alarmwhitelistresponseinfo:

.. table:: **Table 5** AlarmWhiteListResponseInfo

   +-------------------------+-----------------------+------------------------------------------------------------------+
   | Parameter               | Type                  | Description                                                      |
   +=========================+=======================+==================================================================+
   | enterprise_project_name | String                | Enterprise project name                                          |
   +-------------------------+-----------------------+------------------------------------------------------------------+
   | hash                    | String                | Hash value of the event whitelist description (SHA256 algorithm) |
   +-------------------------+-----------------------+------------------------------------------------------------------+
   | description             | String                | Description                                                      |
   +-------------------------+-----------------------+------------------------------------------------------------------+
   | event_type              | Integer               | Intrusion type. Its value can be:                                |
   |                         |                       |                                                                  |
   |                         |                       | -  1001: Malware                                                 |
   |                         |                       |                                                                  |
   |                         |                       | -  1010: Rootkit                                                 |
   |                         |                       |                                                                  |
   |                         |                       | -  1011: Ransomware                                              |
   |                         |                       |                                                                  |
   |                         |                       | -  1015: Web shell                                               |
   |                         |                       |                                                                  |
   |                         |                       | -  1017: Reverse shell                                           |
   |                         |                       |                                                                  |
   |                         |                       | -  2001: Common vulnerability exploit                            |
   |                         |                       |                                                                  |
   |                         |                       | -  3002: File privilege escalation                               |
   |                         |                       |                                                                  |
   |                         |                       | -  3003: Process privilege escalation                            |
   |                         |                       |                                                                  |
   |                         |                       | -  3004: Important file change                                   |
   |                         |                       |                                                                  |
   |                         |                       | -  3005: File/Directory change                                   |
   |                         |                       |                                                                  |
   |                         |                       | -  3007: Abnormal process behavior                               |
   |                         |                       |                                                                  |
   |                         |                       | -  3015: High-risk command execution                             |
   |                         |                       |                                                                  |
   |                         |                       | -  3018: Abnormal shell                                          |
   |                         |                       |                                                                  |
   |                         |                       | -  3027: Suspicious crontab tasks                                |
   |                         |                       |                                                                  |
   |                         |                       | -  4002: Brute-force attack                                      |
   |                         |                       |                                                                  |
   |                         |                       | -  4004: Abnormal login                                          |
   |                         |                       |                                                                  |
   |                         |                       | -  4006: Invalid system account                                  |
   +-------------------------+-----------------------+------------------------------------------------------------------+
   | update_time             | Long                  | Time when the event whitelist is updated, in milliseconds.       |
   |                         |                       |                                                                  |
   |                         |                       | Minimum: **0**                                                   |
   |                         |                       |                                                                  |
   |                         |                       | Maximum: **9223372036854775807**                                 |
   +-------------------------+-----------------------+------------------------------------------------------------------+

Example Requests
----------------

Query the first 10 alarm whitelists whose enterprise project is xxx.

.. code-block:: text

   GET https://{endpoint}/v5/{project_id}/event/white-list/alarm?limit=10&offset=0&enterprise_project_id=xxx

Example Responses
-----------------

**Status code: 200**

Alarm whitelist

.. code-block::

   {
     "data_list" : [ {
       "enterprise_project_name" : "All projects",
       "event_type" : 1001,
       "hash" : "9ab079e5398cba3a368ccffbd478f54c5ec3edadf6284ec049a73c36419f1178",
       "description" : "/opt/cloud/3rdComponent/install/jre-8u201/bin/java",
       "update_time" : 1665715677307
     } ],
     "event_type_list" : [ 1001 ],
     "total_num" : 1
   }

Status Codes
------------

=========== ===============
Status Code Description
=========== ===============
200         Alarm whitelist
=========== ===============

Error Codes
-----------

See :ref:`Error Codes <errorcode>`.

:original_name: ShowAssetStatistic.html

.. _ShowAssetStatistic:

Collecting Asset Statistics, Including Accounts, Ports, and Processes
=====================================================================

Function
--------

This API is used to collect statistics on assets, such as accounts, ports, and processes.

URI
---

GET /v5/{project_id}/asset/statistics

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
   |                       |                 |                 | Minimum: **0**                                                                                                                                                |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Maximum: **128**                                                                                                                                              |
   +-----------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | host_id               | No              | String          | Host ID                                                                                                                                                       |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Minimum: **1**                                                                                                                                                |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Maximum: **128**                                                                                                                                              |
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

   +-----------------------+-----------------------+----------------------------------+
   | Parameter             | Type                  | Description                      |
   +=======================+=======================+==================================+
   | account_num           | Long                  | Number of server accounts        |
   |                       |                       |                                  |
   |                       |                       | Minimum: **0**                   |
   |                       |                       |                                  |
   |                       |                       | Maximum: **2147483647**          |
   +-----------------------+-----------------------+----------------------------------+
   | port_num              | Long                  | Number of open ports             |
   |                       |                       |                                  |
   |                       |                       | Minimum: **0**                   |
   |                       |                       |                                  |
   |                       |                       | Maximum: **2147483647**          |
   +-----------------------+-----------------------+----------------------------------+
   | process_num           | Long                  | Number of processes              |
   |                       |                       |                                  |
   |                       |                       | Minimum: **0**                   |
   |                       |                       |                                  |
   |                       |                       | Maximum: **2147483647**          |
   +-----------------------+-----------------------+----------------------------------+
   | app_num               | Long                  | Pieces of software               |
   |                       |                       |                                  |
   |                       |                       | Minimum: **0**                   |
   |                       |                       |                                  |
   |                       |                       | Maximum: **2147483647**          |
   +-----------------------+-----------------------+----------------------------------+
   | auto_launch_num       | Long                  | Number of auto-startup processes |
   |                       |                       |                                  |
   |                       |                       | Minimum: **0**                   |
   |                       |                       |                                  |
   |                       |                       | Maximum: **2147483647**          |
   +-----------------------+-----------------------+----------------------------------+
   | web_framework_num     | Long                  | Number of web frameworks         |
   |                       |                       |                                  |
   |                       |                       | Minimum: **0**                   |
   |                       |                       |                                  |
   |                       |                       | Maximum: **2147483647**          |
   +-----------------------+-----------------------+----------------------------------+
   | web_site_num          | Long                  | Number of websites               |
   |                       |                       |                                  |
   |                       |                       | Minimum: **0**                   |
   |                       |                       |                                  |
   |                       |                       | Maximum: **2147483647**          |
   +-----------------------+-----------------------+----------------------------------+
   | jar_package_num       | Long                  | Number of JAR packages           |
   |                       |                       |                                  |
   |                       |                       | Minimum: **0**                   |
   |                       |                       |                                  |
   |                       |                       | Maximum: **2147483647**          |
   +-----------------------+-----------------------+----------------------------------+
   | kernel_module_num     | Long                  | Number of kernel modules         |
   |                       |                       |                                  |
   |                       |                       | Minimum: **0**                   |
   |                       |                       |                                  |
   |                       |                       | Maximum: **2147483647**          |
   +-----------------------+-----------------------+----------------------------------+
   | web_service_num       | Long                  | Number of web services           |
   |                       |                       |                                  |
   |                       |                       | Minimum: **0**                   |
   |                       |                       |                                  |
   |                       |                       | Maximum: **2147483647**          |
   +-----------------------+-----------------------+----------------------------------+
   | web_app_num           | Long                  | Number of web applications       |
   |                       |                       |                                  |
   |                       |                       | Minimum: **0**                   |
   |                       |                       |                                  |
   |                       |                       | Maximum: **2147483647**          |
   +-----------------------+-----------------------+----------------------------------+
   | database_num          | Long                  | Number of databases              |
   |                       |                       |                                  |
   |                       |                       | Minimum: **0**                   |
   |                       |                       |                                  |
   |                       |                       | Maximum: **2147483647**          |
   +-----------------------+-----------------------+----------------------------------+

Example Requests
----------------

This API is used to query the fingerprint information, accounts, ports, and processes of a server.

.. code-block:: text

   GET https://{endpoint}/v5/{project_id}/asset/statistics?category=host

Example Responses
-----------------

**Status code: 200**

Asset statistic info

.. code-block::

   {
     "account_num" : 5,
     "port_num" : 5,
     "process_num" : 5,
     "app_num" : 5,
     "auto_launch_num" : 5,
     "web_framework_num" : 5,
     "web_site_num" : 5,
     "jar_package_num" : 5,
     "kernel_module_num" : 5,
     "database_num" : 1,
     "web_app_num" : 8,
     "web_service_num" : 2
   }

Status Codes
------------

=========== ====================
Status Code Description
=========== ====================
200         Asset statistic info
=========== ====================

Error Codes
-----------

See :ref:`Error Codes <errorcode>`.

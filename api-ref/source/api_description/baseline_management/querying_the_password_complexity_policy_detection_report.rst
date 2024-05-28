:original_name: ListPasswordComplexity.html

.. _ListPasswordComplexity:

Querying the Password Complexity Policy Detection Report
========================================================

Function
--------

This API is used to query the password complexity policy detection report.

URI
---

GET /v5/{project_id}/baseline/password-complexity

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
   |                       |                 |                 | Maximum: **256**                                                                                                                                              |
   +-----------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | host_name             | No              | String          | Server name                                                                                                                                                   |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Minimum: **0**                                                                                                                                                |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Maximum: **128**                                                                                                                                              |
   +-----------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | host_ip               | No              | String          | Server IP address                                                                                                                                             |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Minimum: **0**                                                                                                                                                |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Maximum: **128**                                                                                                                                              |
   +-----------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | host_id               | No              | String          | Host ID. If this parameter is not specified, all hosts of a user are queried.                                                                                 |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Minimum: **0**                                                                                                                                                |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Maximum: **128**                                                                                                                                              |
   +-----------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | limit                 | No              | Integer         | Number of records on each page.                                                                                                                               |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Minimum: **0**                                                                                                                                                |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Maximum: **200**                                                                                                                                              |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Default: **10**                                                                                                                                               |
   +-----------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | offset                | No              | Integer         | Offset, which specifies the start position of the record to be returned.                                                                                      |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Minimum: **0**                                                                                                                                                |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Maximum: **2000000**                                                                                                                                          |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Default: **0**                                                                                                                                                |
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

   +-----------------------+----------------------------------------------------------------------------------------------------------------+----------------------------------------------+
   | Parameter             | Type                                                                                                           | Description                                  |
   +=======================+================================================================================================================+==============================================+
   | total_num             | Long                                                                                                           | Total number of password complexity policies |
   |                       |                                                                                                                |                                              |
   |                       |                                                                                                                | Minimum: **0**                               |
   |                       |                                                                                                                |                                              |
   |                       |                                                                                                                | Maximum: **2147483647**                      |
   +-----------------------+----------------------------------------------------------------------------------------------------------------+----------------------------------------------+
   | data_list             | Array of :ref:`PwdPolicyInfoResponseInfo <listpasswordcomplexity__response_pwdpolicyinforesponseinfo>` objects | List of password complexity policy detection |
   |                       |                                                                                                                |                                              |
   |                       |                                                                                                                | Array Length: **0 - 2147483647**             |
   +-----------------------+----------------------------------------------------------------------------------------------------------------+----------------------------------------------+

.. _listpasswordcomplexity__response_pwdpolicyinforesponseinfo:

.. table:: **Table 5** PwdPolicyInfoResponseInfo

   +-----------------------+-----------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Parameter             | Type                  | Description                                                                                                                                                                                                                        |
   +=======================+=======================+====================================================================================================================================================================================================================================+
   | host_id               | String                | Host ID                                                                                                                                                                                                                            |
   |                       |                       |                                                                                                                                                                                                                                    |
   |                       |                       | Minimum: **0**                                                                                                                                                                                                                     |
   |                       |                       |                                                                                                                                                                                                                                    |
   |                       |                       | Maximum: **64**                                                                                                                                                                                                                    |
   +-----------------------+-----------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | host_name             | String                | Server name                                                                                                                                                                                                                        |
   |                       |                       |                                                                                                                                                                                                                                    |
   |                       |                       | Minimum: **0**                                                                                                                                                                                                                     |
   |                       |                       |                                                                                                                                                                                                                                    |
   |                       |                       | Maximum: **256**                                                                                                                                                                                                                   |
   +-----------------------+-----------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | host_ip               | String                | Server IP address                                                                                                                                                                                                                  |
   |                       |                       |                                                                                                                                                                                                                                    |
   |                       |                       | Minimum: **0**                                                                                                                                                                                                                     |
   |                       |                       |                                                                                                                                                                                                                                    |
   |                       |                       | Maximum: **256**                                                                                                                                                                                                                   |
   +-----------------------+-----------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | min_length            | Boolean               | Indicates whether the minimum password length meets the requirements. If the value is true, the minimum password length meets the requirements. If the value is false, the minimum password length does not meet the requirements. |
   +-----------------------+-----------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | uppercase_letter      | Boolean               | Indicates whether the uppercase letters meet the requirements. If the value is true, the uppercase letters meet the requirements. If the value is false, the uppercase letters do not meet the requirements.                       |
   +-----------------------+-----------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | lowercase_letter      | Boolean               | Indicates whether the lowercase letters meet the requirements. If the value is true, the lowercase letters meet the requirements. If the value is false, the lowercase letters do not meet the requirements.                       |
   +-----------------------+-----------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | number                | Boolean               | Indicates whether the number meets the requirements. If the value is true, the number meets the requirements. If the value is false, the number does not meet the requirements.                                                    |
   +-----------------------+-----------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | special_character     | Boolean               | Indicates whether the special character meets the requirements. If the value is true, the special character meets the requirements. If the value is false, the special character does not meet the requirements.                   |
   +-----------------------+-----------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | suggestion            | String                | Modification suggestion                                                                                                                                                                                                            |
   |                       |                       |                                                                                                                                                                                                                                    |
   |                       |                       | Minimum: **0**                                                                                                                                                                                                                     |
   |                       |                       |                                                                                                                                                                                                                                    |
   |                       |                       | Maximum: **65534**                                                                                                                                                                                                                 |
   +-----------------------+-----------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Example Requests
----------------

Query the password complexity of the server whose enterprise project ID is xxx. Data on the first page (the first 10 records) is returned by default.

.. code-block:: text

   GET https://{endpoint}/v5/{project_id}/baseline/password-complexity?enterprise_project_id=xxx

Example Responses
-----------------

**Status code: 200**

password complexity policy check report

.. code-block::

   {
     "total_num" : 1,
     "data_list" : [ {
       "host_id" : "76fa440a-5a08-43fa-ac11-d12183ab3a14",
       "host_ip" : "192.168.0.59",
       "host_name" : "ecs-6b96",
       "lowercase_letter" : false,
       "min_length" : true,
       "number" : false,
       "special_character" : false,
       "suggestion" : "The password should contain at least 3 of the following character types: uppercase letters, lowercase letters, digits, and special characters. ",
       "uppercase_letter" : false
     } ]
   }

Status Codes
------------

=========== =======================================
Status Code Description
=========== =======================================
200         password complexity policy check report
=========== =======================================

Error Codes
-----------

See :ref:`Error Codes <errorcode>`.

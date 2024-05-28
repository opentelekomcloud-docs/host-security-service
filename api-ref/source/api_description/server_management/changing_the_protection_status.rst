:original_name: SwitchHostsProtectStatus.html

.. _SwitchHostsProtectStatus:

Changing the Protection Status
==============================

Function
--------

This API is used to change the protection status.

URI
---

POST /v5/{project_id}/host-management/protection

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

.. table:: **Table 4** Request body parameters

   +-----------------+-----------------+-----------------------------------------------------------------------------+-----------------------------------------------+
   | Parameter       | Mandatory       | Type                                                                        | Description                                   |
   +=================+=================+=============================================================================+===============================================+
   | version         | No              | String                                                                      | HSS edition. Its value can be:                |
   |                 |                 |                                                                             |                                               |
   |                 |                 |                                                                             | -  hss.version.null: protection disabled      |
   |                 |                 |                                                                             |                                               |
   |                 |                 |                                                                             | -  hss.version.enterprise: enterprise edition |
   |                 |                 |                                                                             |                                               |
   |                 |                 |                                                                             | -  hss.version.premium: premium edition       |
   +-----------------+-----------------+-----------------------------------------------------------------------------+-----------------------------------------------+
   | charging_mode   | No              | String                                                                      | on_demand: pay-per-use                        |
   +-----------------+-----------------+-----------------------------------------------------------------------------+-----------------------------------------------+
   | resource_id     | No              | String                                                                      | Instance ID                                   |
   |                 |                 |                                                                             |                                               |
   |                 |                 |                                                                             | Minimum: **1**                                |
   |                 |                 |                                                                             |                                               |
   |                 |                 |                                                                             | Maximum: **128**                              |
   +-----------------+-----------------+-----------------------------------------------------------------------------+-----------------------------------------------+
   | host_id_list    | No              | Array of strings                                                            | Server list                                   |
   |                 |                 |                                                                             |                                               |
   |                 |                 |                                                                             | Minimum: **1**                                |
   |                 |                 |                                                                             |                                               |
   |                 |                 |                                                                             | Maximum: **128**                              |
   |                 |                 |                                                                             |                                               |
   |                 |                 |                                                                             | Array Length: **0 - 2097152**                 |
   +-----------------+-----------------+-----------------------------------------------------------------------------+-----------------------------------------------+
   | tags            | No              | Array of :ref:`TagInfo <switchhostsprotectstatus__request_taginfo>` objects | Resource tag                                  |
   |                 |                 |                                                                             |                                               |
   |                 |                 |                                                                             | Array Length: **0 - 2097152**                 |
   +-----------------+-----------------+-----------------------------------------------------------------------------+-----------------------------------------------+

.. _switchhostsprotectstatus__request_taginfo:

.. table:: **Table 5** TagInfo

   +-----------------+-----------------+-----------------+---------------------------------------------------------------------------------+
   | Parameter       | Mandatory       | Type            | Description                                                                     |
   +=================+=================+=================+=================================================================================+
   | key             | No              | String          | Key. It can contain up to 128 Unicode characters. The key cannot be left blank. |
   |                 |                 |                 |                                                                                 |
   |                 |                 |                 | Minimum: **1**                                                                  |
   |                 |                 |                 |                                                                                 |
   |                 |                 |                 | Maximum: **128**                                                                |
   +-----------------+-----------------+-----------------+---------------------------------------------------------------------------------+
   | value           | No              | String          | Value. Each tag value can contain a maximum of 255 Unicode characters.          |
   |                 |                 |                 |                                                                                 |
   |                 |                 |                 | Minimum: **1**                                                                  |
   |                 |                 |                 |                                                                                 |
   |                 |                 |                 | Maximum: **255**                                                                |
   +-----------------+-----------------+-----------------+---------------------------------------------------------------------------------+

Response Parameters
-------------------

None

Example Requests
----------------

Switch the protection edition of the server whose ID is 71a15ecc-049f-4cca-bd28-5e90aca1817f to the enterprise edition.

.. code-block::

   {
     "version" : "hss.version.enterprise",
     "charging_mode" : "on_demand",
     "resource_id" : "af4d08ad-2b60-4916-a5cf-8d6a23956dda",
     "host_id_list" : [ "71a15ecc-049f-4cca-bd28-5e90aca1817f" ],
     "tags" : [ {
       "key" : "Service",
       "value" : "hss"
     } ]
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

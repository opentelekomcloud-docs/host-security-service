:original_name: ListPolicyGroup.html

.. _ListPolicyGroup:

Querying the Policy Group List
==============================

Function
--------

This API is used to query the policy group list.

URI
---

GET /v5/{project_id}/policy/groups

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
   | group_name            | No              | String          | Policy group name                                                                                                                                             |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Minimum: **1**                                                                                                                                                |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Maximum: **256**                                                                                                                                              |
   +-----------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | offset                | No              | Integer         | Offset, which specifies the start position of the record to be returned.                                                                                      |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Minimum: **0**                                                                                                                                                |
   |                       |                 |                 |                                                                                                                                                               |
   |                       |                 |                 | Maximum: **100000**                                                                                                                                           |
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

   +-----------------------+-----------------------------------------------------------------------------------------------------+---------------------------+
   | Parameter             | Type                                                                                                | Description               |
   +=======================+=====================================================================================================+===========================+
   | total_num             | Integer                                                                                             | Total number              |
   +-----------------------+-----------------------------------------------------------------------------------------------------+---------------------------+
   | data_list             | Array of :ref:`PolicyGroupResponseInfo <listpolicygroup__response_policygroupresponseinfo>` objects | Policy group list         |
   |                       |                                                                                                     |                           |
   |                       |                                                                                                     | Array Length: **0 - 100** |
   +-----------------------+-----------------------------------------------------------------------------------------------------+---------------------------+

.. _listpolicygroup__response_policygroupresponseinfo:

.. table:: **Table 5** PolicyGroupResponseInfo

   +-----------------------+-----------------------+----------------------------------------------------------------------------+
   | Parameter             | Type                  | Description                                                                |
   +=======================+=======================+============================================================================+
   | group_name            | String                | Policy group name                                                          |
   +-----------------------+-----------------------+----------------------------------------------------------------------------+
   | group_id              | String                | Policy group ID                                                            |
   +-----------------------+-----------------------+----------------------------------------------------------------------------+
   | description           | String                | Description of the policy group                                            |
   |                       |                       |                                                                            |
   |                       |                       | Minimum: **1**                                                             |
   |                       |                       |                                                                            |
   |                       |                       | Maximum: **64**                                                            |
   +-----------------------+-----------------------+----------------------------------------------------------------------------+
   | deletable             | Boolean               | Whether a policy group can be deleted                                      |
   |                       |                       |                                                                            |
   |                       |                       | -  true: The policy group can be deleted.                                  |
   |                       |                       |                                                                            |
   |                       |                       | -  false: The policy group cannot be deleted.                              |
   +-----------------------+-----------------------+----------------------------------------------------------------------------+
   | host_num              | Integer               | Number of associated servers                                               |
   +-----------------------+-----------------------+----------------------------------------------------------------------------+
   | default_group         | Boolean               | Whether a policy group is the default policy group                         |
   |                       |                       |                                                                            |
   |                       |                       | -  true: The policy group is the default policy group.                     |
   |                       |                       |                                                                            |
   |                       |                       | -  false: The policy group is not the default policy group.                |
   +-----------------------+-----------------------+----------------------------------------------------------------------------+
   | support_os            | String                | Supported OS. The options are as follows:                                  |
   |                       |                       |                                                                            |
   |                       |                       | -  Linux                                                                   |
   |                       |                       |                                                                            |
   |                       |                       | -  Windows                                                                 |
   +-----------------------+-----------------------+----------------------------------------------------------------------------+
   | support_version       | String                | Supported versions. The options are as follows:                            |
   |                       |                       |                                                                            |
   |                       |                       | -  hss.version.enterprise: policy group of the enterprise edition          |
   |                       |                       |                                                                            |
   |                       |                       | -  hss.version.premium: policy group of the premium edition                |
   |                       |                       |                                                                            |
   |                       |                       | -  hss.version.container.enterprise: policy group of the container edition |
   +-----------------------+-----------------------+----------------------------------------------------------------------------+

Example Requests
----------------

Query the policy group list of all enterprise projects.

.. code-block:: text

   GET https://{endpoint}/v5/{project_id}/policy/groups?offset=0&limit=100&enterprise_project_id=all_granted_eps

Example Responses
-----------------

**Status code: 200**

Policy group list

.. code-block::

   {
     "data_list" : [ {
       "default_group" : true,
       "deletable" : false,
       "description" : "container policy group for linux",
       "group_id" : "c831f177-226d-4b91-be0f-bcf98d04ef5d",
       "group_name" : "tenant_linux_container_default_policy_group ",
       "host_num" : 0,
       "support_version" : "hss.version.container.enterprise",
       "support_os" : "Linux"
     }, {
       "default_group" : true,
       "deletable" : false,
       "description" : "enterprise policy group for windows",
       "group_id" : "1ff54b90-1b3e-42a9-a1da-9883a83385ce",
       "group_name" : "tenant_windows_enterprise_default_policy_group ",
       "host_num" : 0,
       "support_version" : "hss.version.enterprise",
       "support_os" : "Windows"
     }, {
       "default_group" : true,
       "deletable" : false,
       "description" : "enterprise policy group for linux",
       "group_id" : "1069bcc0-c806-4ccd-a35d-f1f7456805e9",
       "group_name" : "tenant_linux_enterprise_default_policy_group ",
       "host_num" : 1,
       "support_version" : "hss.version.enterprise",
       "support_os" : "Linux"
     }, {
       "default_group" : true,
       "deletable" : false,
       "description" : "premium policy group for windows",
       "group_id" : "11216d24-9e91-4a05-9212-c4c1d646ee79",
       "group_name" : "tenant_windows_premium_default_policy_group ",
       "host_num" : 0,
       "support_version" : "hss.version.premium",
       "support_os" : "Linux"
     }, {
       "default_group" : true,
       "deletable" : false,
       "description" : "premium policy group for linux",
       "group_id" : "e6e1228a-7bb4-424f-a42b-755162234da7",
       "group_name" : "tenant_linux_premium_default_policy_group ",
       "host_num" : 0,
       "support_version" : "hss.version.premium",
       "support_os" : "Windows"
     } ],
     "total_num" : 5
   }

Status Codes
------------

=========== =================
Status Code Description
=========== =================
200         Policy group list
=========== =================

Error Codes
-----------

See :ref:`Error Codes <errorcode>`.

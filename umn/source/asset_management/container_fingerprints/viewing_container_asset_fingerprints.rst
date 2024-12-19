:original_name: hss_01_0465.html

.. _hss_01_0465:

Viewing Container Asset Fingerprints
====================================

HSS can collect container asset fingerprints, including container clusters, services, workloads, accounts, ports, and processes. You can centrally check container asset information and detect risky assets in a timely manner based on the container fingerprints.

This section describes how to view collected container asset information. For more information, see :ref:`Collecting Container Asset Fingerprints <hss_01_0478>`.

Constraints
-----------

-  Only the HSS container edition supports the container fingerprint function.
-  Only Linux is supported.

Viewing Asset Fingerprints Data of All Containers
-------------------------------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. Choose **Asset Management** > **Container Fingerprints** > **Asset Fingerprints**. On the **Asset Fingerprints** page that is displayed, view the fingerprint data of all containers.

   .. note::

      If your servers are managed by enterprise projects, you can select the target enterprise project to view or operate the asset and detection information.


   .. figure:: /_static/images/en-us_image_0000001853723125.png
      :alt: **Figure 1** Viewing container assets

      **Figure 1** Viewing container assets

#. Click a fingerprint type in the list to view the asset information.

#. (Optional) Remove risky assets.

   If you find unsafe assets after counting, remove them in a timely manner.

   You are advised to handle unsafe ports as follows:

   -  If HSS detects open high-risk ports or unused ports, check whether they are really used by your services. If they are not, disable them. For dangerous ports, you are advised to further check their program files, and delete or isolate their source files if necessary.
   -  If a detected high-risk port is actually a normal port used for services, you can ignore it. Ignored alarms will neither be recorded as unsafe items and nor trigger alarms.

Viewing Asset Fingerprint Data of a Single Container
----------------------------------------------------

#. Log in to the management console.

#. Click |image2| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane, choose **Asset Management** > **Servers & Quota**. Click the **Servers** tab.

   .. note::

      If your servers are managed by enterprise projects, you can select an enterprise project to view or operate the asset and scan information.

#. Click the name of the target server. On the server details page that is displayed, choose **Asset Fingerprints** > **Containers**.

#. Click a fingerprint type in the list to view the asset information.

#. (Optional) Remove risky assets.

   If you find unsafe assets after counting, remove them in a timely manner.

   You are advised to handle unsafe ports as follows:

   -  If HSS detects open high-risk ports or unused ports, check whether they are really used by your services. If they are not, disable them. For dangerous ports, you are advised to further check their program files, and delete or isolate their source files if necessary.
   -  If a detected high-risk port is actually a normal port used for services, you can ignore it. Ignored alarms will neither be recorded as unsafe items and nor trigger alarms.

Viewing Cluster Information
---------------------------

#. Log in to the management console.

#. Click |image3| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane, choose **Asset Management** > **Container Fingerprints**.

#. Choose **Clusters** and click **Synchronize** in the upper left corner.

#. **Last Synchronized** indicates the CCE cluster, service, workload, and container data is synchronized successfully.

#. On the **Clusters** page, view cluster information.

   The **Clusters** page displays the cluster name, type, node, version, creation time, and status.

   -  Searching for the target cluster

      You can enter information such as the cluster name and status in the search box to search for the target cluster.

   -  Viewing details about the target cluster

      a. Click the name of the target cluster to go to the CCE console.
      b. On the CCE console, view basic cluster information and network information.

Viewing Services
----------------

#. Log in to the management console.

#. Click |image4| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane, choose **Asset Management** > **Container Fingerprints**.

#. Choose **Clusters** and click **Synchronize** in the upper left corner.

#. **Last Synchronized** indicates the CCE cluster, service, workload, and container data is synchronized successfully.

#. On the **Services** tab page, view the information.

   The page displays the service name, endpoint name, access mode, service IP address, namespace, cluster name, and creation time.

   -  Searching for a service

      You can enter information such as the service name and access mode in the search box to search for the service.

   -  Viewing details about a service

      Click the name of a service. On the service details page that is displayed, you can view the selector, tag, and port of the service.

Viewing Endpoints
-----------------

#. Log in to the management console.

#. Click |image5| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane, choose **Asset Management** > **Container Fingerprints**.

#. Choose **Clusters** and click **Synchronize** in the upper left corner.

#. **Last Synchronized** indicates the CCE cluster, service, workload, and container data is synchronized successfully.

#. Choose **Services** > **Endpoints**. View endpoints information.

   The page displays the endpoint name, namespace, cluster associated with service, service name, and creation time.

   -  Searching for an endpoint

      You can enter information such as the endpoint name and namespace in the search box to search for the endpoint.

   -  Viewing details about an endpoint

      Click the name of an endpoint. On the endpoint details page that is displayed, you can view the pod mapping and port information.

Viewing a Workload
------------------

#. Log in to the management console.

#. Click |image6| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane, choose **Asset Management** > **Container Fingerprints**.

#. Choose **Clusters** and click **Synchronize** in the upper left corner.

#. **Last Synchronized** indicates the CCE cluster, service, workload, and container data is synchronized successfully.

#. Click the **Workloads** tab.

#. Select different workloads and view information.

   You can view information about **Deployment**, **StatefulSets**, **DaemonSets**, **Jobs**, **Cron Jobs**, and **Pods**. For details about the information items, see :ref:`Workload information Items <hss_01_0465__table1923713515214>`.

   You can enter information such as the workload name and cluster in the search box to search for the target workload.

   .. _hss_01_0465__table1923713515214:

   .. table:: **Table 1** Workload information

      +-----------------------------------+-----------------------------------+
      | Workload Type                     | Item                              |
      +===================================+===================================+
      | Deployment                        | -  Workload name                  |
      |                                   | -  Status                         |
      |                                   | -  Instances                      |
      |                                   | -  Namespaces                     |
      |                                   | -  Created                        |
      |                                   | -  Image name                     |
      |                                   | -  Cluster                        |
      +-----------------------------------+-----------------------------------+
      | StatefulSets                      | -  Workload name                  |
      |                                   | -  Status                         |
      |                                   | -  Instances                      |
      |                                   | -  Namespace                      |
      |                                   | -  Created                        |
      |                                   | -  Image name                     |
      |                                   | -  Cluster                        |
      +-----------------------------------+-----------------------------------+
      | DaemonSets                        | -  Workload name                  |
      |                                   | -  Status                         |
      |                                   | -  Instances                      |
      |                                   | -  Namespace                      |
      |                                   | -  Created                        |
      |                                   | -  Image name                     |
      |                                   | -  Cluster                        |
      +-----------------------------------+-----------------------------------+
      | Jobs                              | -  Workload name                  |
      |                                   | -  Status                         |
      |                                   | -  Instances                      |
      |                                   | -  Namespace                      |
      |                                   | -  Created                        |
      |                                   | -  Image name                     |
      |                                   | -  Cluster                        |
      +-----------------------------------+-----------------------------------+
      | Cron Jobs                         | -  Workload name                  |
      |                                   | -  Status                         |
      |                                   | -  Trigger                        |
      |                                   | -  Running jobs                   |
      |                                   | -  Namespace                      |
      |                                   | -  Latest scheduled               |
      |                                   | -  Created                        |
      |                                   | -  Image name                     |
      |                                   | -  Cluster                        |
      +-----------------------------------+-----------------------------------+
      | Pods                              | -  Name                           |
      |                                   | -  Namespace                      |
      |                                   | -  Cluster                        |
      |                                   | -  Node                           |
      |                                   | -  Pod IP address                 |
      |                                   | -  POD IP                         |
      |                                   | -  Status                         |
      |                                   | -  Created                        |
      +-----------------------------------+-----------------------------------+

Viewing Container Instances
---------------------------

#. Log in to the management console.

#. In the navigation pane, choose **Asset Management** > **Container Fingerprints**.

#. Choose **Clusters** and click **Synchronize** in the upper left corner.

#. **Last Synchronized** indicates the CCE cluster, service, workload, and container data is synchronized successfully.

#. Click the **Container Instances** tab.

   The container name, status, pod, cluster name, creation time, and image name are displayed.

   -  Searching for a container

      You can enter information such as the container name and status in the search box to search for the container.

   -  Viewing details about a container

      Click the name of a container. On the container details page that is displayed, you can view the process, port, and mount path.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png
.. |image2| image:: /_static/images/en-us_image_0000001517477398.png
.. |image3| image:: /_static/images/en-us_image_0000001517477398.png
.. |image4| image:: /_static/images/en-us_image_0000001517477398.png
.. |image5| image:: /_static/images/en-us_image_0000001517477398.png
.. |image6| image:: /_static/images/en-us_image_0000001517477398.png

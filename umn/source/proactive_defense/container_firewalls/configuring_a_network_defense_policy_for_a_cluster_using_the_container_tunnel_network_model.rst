:original_name: hss_01_0623.html

.. _hss_01_0623:

Configuring a Network Defense Policy (for a Cluster Using the Container Tunnel Network Model)
=============================================================================================

You can configure network defense policies to limit the access traffic to the pods in a cluster using the container tunnel network model. If no network policies are configured, all the inbound and outbound traffic of the pods in a namespace are allowed by default.

This section describes how to configure a network policy for a cluster using the container tunnel network model.

Constraints
-----------

-  Only clusters that use the tunnel network model support network policies. Network policies are classified into the following types:

   -  Inbound rules, which are supported by all cluster versions.
   -  Outbound rules, which are supported only by clusters in version 1.23 and later.

-  Network isolation is not supported for IPv6 addresses.

Creating a Network Policy from YAML
-----------------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane on the left, choose **Prevention** > **Container Firewalls**.

#. Click **Synchronize** above the cluster list to synchronize the policies created on CCE.

   The task takes about 1 to 2 minutes. Wait for a while and click |image2| in the upper right corner of the list to refresh and view the latest data.

#. Click **Manage Policy** in the **Operation** column of a cluster using the container tunnel network model.

#. Click **Create from YAML** above the policy list.

#. On the YAML creation page, enter content or click **Import**.

   An example of a network policy created from YAML is as follows:

   .. code-block::

      apiVersion: networking.k8s.io/v1
      kind: NetworkPolicy
      metadata:
        name: test-network-policy
        namespace: default
      spec:
        podSelector:                  # The rule takes effect for pods with the role=db label.
          matchLabels:
            role: db
        policyTypes:
          - Ingress
          - Egress
        ingress:                      # Ingress rule
          - from:
              - namespaceSelector: # Only namespaces with project=myproject can be accessed.
                  matchLabels:
                    project: myproject
              - podSelector:              # Only the traffic from the pods with the role=frontend label is allowed.
                  matchLabels:
                    role: frontend
            ports                       # Only TCP can be used to access port 6379.
              - protocol: TCP
                port: 6379
        egress:                         # Egress rule
          - to:
              - ipBlock:                #Only the 10.0.0.0/24 network segment of the destination object can be accessed.
                  cidr: 10.0.0.0/24
            ports:                      # Only TCP can be used to access port 6379 of the destination object.
              - protocol: TCP
                port: 6379

#. Click **OK**.

Creating a Network Policy on the GUI
------------------------------------

#. Log in to the management console.
#. In the navigation pane on the left, choose **Prevention** > **Container Firewalls**.
#. Click **Manage Policy** in the **Operation** column of a cluster using the container tunnel network model.
#. Click **Create Network Policy** above the network policy list.

   -  **Policy Name**: Enter a network policy name.

   -  **Namespace**: Select a namespace for the network policy.

   -  **Selector**: Enter a key and a value to set the pod to be associated, and click **Add**. You can also click **Reference Workload Label** to reference the label of an existing workload. If this parameter is not specified, all pods in the namespace are associated by default.

   -  Inbound rule: Click **Add Rule** in the **Inbound Rules** area. For more information, see :ref:`Table 1 <hss_01_0623__hss_01_0501_table32391930185612>`.

      .. _hss_01_0623__hss_01_0501_table32391930185612:

      .. table:: **Table 1** Adding an inbound rule

         +------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
         | Parameter        | Description                                                                                                                                                                            |
         +==================+========================================================================================================================================================================================+
         | Protocol & Port  | Enter the inbound protocol type and port number of the pods to be associated. Currently, TCP and UDP are supported. If this parameter is not specified, all access traffic is allowed. |
         +------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
         | Source Namespace | Select a namespace whose objects can be accessed. If this parameter is not specified, access to the objects that belong to the same namespace as the current policy is allowed.        |
         +------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
         | Source Pod Label | Select a label. Pods with this label can be accessed. If this parameter is not specified, all pods in the namespace can be accessed.                                                   |
         +------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

   -  Outbound rule: Click **Add Rule** in the **Outbound Rules** area. For more information, see :ref:`Table 2 <hss_01_0623__hss_01_0501_table13434025124710>`.

      .. _hss_01_0623__hss_01_0501_table13434025124710:

      .. table:: **Table 2** Adding an outbound rule

         +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------+
         | Parameter                         | Description                                                                                                                                    |
         +===================================+================================================================================================================================================+
         | Protocol & Port                   | Enter the port and protocol of destination objects. If this parameter is not specified, access is not limited.                                 |
         +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------+
         | Destination CIDR Block            | Configure CIDR blocks. This parameter allows requests to be routed to a specified CIDR block (and not to the exception CIDR blocks).           |
         |                                   |                                                                                                                                                |
         |                                   | Separate the destination and exception CIDR blocks by vertical bars (|), and separate multiple exception CIDR blocks by commas (,).            |
         |                                   |                                                                                                                                                |
         |                                   | For example, 172.17.0.0/16|172.17.1.0/24,172.17.2.0/24 indicates that 172.17.0.0/16 is accessible, but not for 172.17.1.0/24 or 172.17.2.0/24. |
         +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------+
         | Destination Namespace             | Namespace where the destination object is located. If not specified, the object belongs to the same namespace as the current policy.           |
         +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------+
         | Destination Pod Label             | Select a label. Pods with this label can be accessed. If this parameter is not specified, all pods in the namespace can be accessed.           |
         +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------+

5. Click **OK**.

Related Operations
------------------

**Modifying or deleting a network policy**

#. Log in to the HSS console.
#. In the navigation pane on the left, choose **Prevention** > **Container Firewalls**.
#. Click **Manage Policy** in the **Operation** column of a cluster using the container tunnel network model.
#. Click **Synchronize** above the network policy list.
#. Check the value of **Last synchronized**. If it changes to the completion time of the latest synchronization task, the synchronization is complete.
#. Manage policies as needed.

   -  Modifying a policy

      -  In the **Operation** column of a policy, click **Edit YAML**. On the YAML page, modify the YAML content and click **OK**.
      -  In the **Operation** column of a policy, click **Update**. Modify the network policy information and click **OK**.

   -  Deleting a policy

      -  In the **Operation** column of a policy, click **Delete**. In the confirmation dialog box, click **OK**.
      -  Select one or multiple policies and click **Delete** above the policy list. In the displayed dialog box, click **OK**.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png
.. |image2| image:: /_static/images/en-us_image_0000001798922782.png

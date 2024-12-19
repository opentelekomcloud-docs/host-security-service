:original_name: hss_01_0550.html

.. _hss_01_0550:

Installing the Agent in a Cluster
=================================

To install the agent for all nodes in a CCE cluster or an on-premises Kubernetes cluster, you can use the cluster agent management function to install the agent in the cluster. After this function is enabled, you do not need to manually install the agent on new nodes or pods added to the cluster.

Installing an Agent in a CCE Cluster
------------------------------------

#. Log in to the management console.

#. In the navigation pane, choose **Asset Management** > **Containers & Quota**.

#. Click the **Cluster Agents** tab and click **CCE cluster**.

#. In the **Operation** column of a cluster, click **Install Agent**.

   You can also select multiple clusters and click **Install Agent** in the upper left corner of the list.

#. In the dialog box that is displayed, click **OK**.

   It takes about 10 minutes to install the agent. Wait for 10 minutes and move the cursor to the **Agent Installation Status** column to view the status.

Installing an Agent in an On-Premises Cluster
---------------------------------------------

#. Log in to the management console.

#. In the navigation pane, choose **Asset Management** > **Containers & Quota**.

#. Click the **Cluster Agents** tab and click **On-premises cluster**.

#. Click **Add On-Premises Cluster**.

#. In the dialog box that is displayed, enter cluster information and click **Generate Command**.

   In the dialog box that is displayed, click **Save**.

#. Create a YAML file, for example, **abcd.yaml**, on the server where Kubernetes commands can be executed.

#. Copy the generated command to **abcd.yaml**.

#. Run the following command on the server to execute **abcd.yaml** and install the agent. This step takes about 10 minutes.

   **kubectl apply -f abcd.yaml**

#. Return to the HSS console.

#. In the navigation pane, choose **Installation & Configuration**.

#. Click the **Agents** tab. If the agent status of the cluster server is **Online**, the agent has been installed.

Modifying On-premises Cluster Information
-----------------------------------------

-  To modify the on-premises cluster information or view commands, click **Edit** in its **Operation** column.
-  To remove the information about an on-premises cluster, click **Remove** in its **Operation** column.

Follow-up Procedure
-------------------

After the agent is installed, enable protection for the container. For details, see :ref:`Enabling Container Protection <hss_01_0295>`.

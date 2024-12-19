:original_name: hss_01_0632.html

.. _hss_01_0632:

Configuring a Container Cluster Protection Policy
=================================================

You can configure container cluster protection policies to specify the level of risks (unsafe baselines, vulnerabilities, or malicious files) that trigger alarms, cluster protection scope, image whitelist, and the actions taken on an alarm.

Creating a Policy
-----------------

#. Log in to the management console.

2. In the navigation pane, choose **Prevention** > **Container Cluster Protection**.

3. Click the **Protection Policies** tab and click **Create Policy**.

4. Configure parameters in the **Create Policy** dialog box.

   a. Configure a protection policy. The following table describes the parameters.

      .. table:: **Table 1** Container cluster protection policy parameters

         +------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
         | Parameter              | Description                                                                                                                                                                                                                               | Example Value         |
         +========================+===========================================================================================================================================================================================================================================+=======================+
         | Policy Template        | Select a policy template.                                                                                                                                                                                                                 | Default template      |
         +------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
         | Policy Name            | User-defined policy name.                                                                                                                                                                                                                 | test                  |
         +------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
         | Policy Description     | Description about the policy.                                                                                                                                                                                                             | Test                  |
         +------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
         | Block Unscanned Images | Whether to block images that have not been scanned using the HSS container image security function.                                                                                                                                       | |image2|              |
         |                        |                                                                                                                                                                                                                                           |                       |
         |                        | -  |image1|: disable                                                                                                                                                                                                                      |                       |
         +------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
         | Alarm Policy           | Alarm policy type.                                                                                                                                                                                                                        | Malicious script      |
         |                        |                                                                                                                                                                                                                                           |                       |
         |                        | -  **Baseline**                                                                                                                                                                                                                           |                       |
         |                        | -  **Vulnerability**                                                                                                                                                                                                                      |                       |
         |                        | -  **Malicious script**                                                                                                                                                                                                                   |                       |
         +------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
         | Risk Level             | Risk level that triggers an alarm.                                                                                                                                                                                                        | High                  |
         |                        |                                                                                                                                                                                                                                           |                       |
         |                        | -  **High**                                                                                                                                                                                                                               |                       |
         |                        | -  **Medium**                                                                                                                                                                                                                             |                       |
         |                        | -  **Low**                                                                                                                                                                                                                                |                       |
         +------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
         | Baseline Item          | Configure unsafe baseline items. If an image to be started contains any of these items, HSS will take specified actions immediately.                                                                                                      | ``-``                 |
         +------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
         | Vulnerability Item     | Configure vulnerabilities. If an image to be started contains any of these vulnerabilities, HSS will take specified actions immediately.                                                                                                  | ``-``                 |
         +------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
         | Malicious Sample       | Configure malicious samples. If an image to be started contains any of these samples, HSS will take specified actions immediately.                                                                                                        | malwares              |
         +------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
         | Action                 | Action taken by HSS if it detects that an image to be started contains specified unsafe baseline items, vulnerabilities, or malicious scripts.                                                                                            | Block                 |
         |                        |                                                                                                                                                                                                                                           |                       |
         |                        | -  **Alarm**: Generate an event whose **Action** is **Alarm** on the **Protection Events** tab of the **Container Cluster Protection** page.                                                                                              |                       |
         |                        | -  **Block**: Block an unsafe image and generate an event whose **Action** is **Block** on the **Protection Events** tab of the **Container Cluster Protection** page.                                                                    |                       |
         |                        | -  **Allow**: Generate an event whose **Action** is **Allow** on the **Protection Events** tab of the **Container Cluster Protection** page.                                                                                              |                       |
         +------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
         | Add to Whitelist       | Images to be added to the whitelist. Enter values in *ImageName*\ **:**\ *ImageVersion* format. An image name can contain only numbers, letters, underscores (_), hyphens (-), and periods (.). Each image name occupies a separate line. | ``-``                 |
         |                        |                                                                                                                                                                                                                                           |                       |
         |                        | Example:                                                                                                                                                                                                                                  |                       |
         |                        |                                                                                                                                                                                                                                           |                       |
         |                        | -  A single image                                                                                                                                                                                                                         |                       |
         |                        |                                                                                                                                                                                                                                           |                       |
         |                        |    **image:1.0**                                                                                                                                                                                                                          |                       |
         |                        |                                                                                                                                                                                                                                           |                       |
         |                        | -  Multiple images                                                                                                                                                                                                                        |                       |
         |                        |                                                                                                                                                                                                                                           |                       |
         |                        |    **image1:1.0**                                                                                                                                                                                                                         |                       |
         |                        |                                                                                                                                                                                                                                           |                       |
         |                        |    **image2:1.0**                                                                                                                                                                                                                         |                       |
         |                        |                                                                                                                                                                                                                                           |                       |
         |                        | .. important::                                                                                                                                                                                                                            |                       |
         |                        |                                                                                                                                                                                                                                           |                       |
         |                        |    NOTICE:                                                                                                                                                                                                                                |                       |
         |                        |    Exercise caution when performing this operation. HSS does not check whitelisted images when they are started.                                                                                                                          |                       |
         +------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+

   b. Click **Next**.

   c. Configure protection scope.

      Configure the protection scope of clusters, images, and tags.

5. Click **OK**.

   You can view the new protection policy in the policy list.

Editing or Deleting a Cluster Protection Policy
-----------------------------------------------

#. Choose **Container Cluster Protection** and click the **Protection Policies** tab.
#. In the **Operation** column of a policy, click a button as required.

   -  **View YAML**: View the protection policy content in YAML format.
   -  **Edit**: Modify a protection policy.
   -  **Delete**: Delete a protection policy.

   .. important::

      After a policy is deleted, the container clusters associated with it will no be protected. Exercise caution when performing this operation.

#. Click **OK**.

.. |image1| image:: /_static/images/en-us_image_0000001664124710.png
.. |image2| image:: /_static/images/en-us_image_0000002005465025.png

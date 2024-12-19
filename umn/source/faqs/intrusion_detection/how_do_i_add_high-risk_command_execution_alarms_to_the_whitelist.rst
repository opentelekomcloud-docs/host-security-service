:original_name: hss_01_0595.html

.. _hss_01_0595:

How Do I Add High-risk Command Execution Alarms to the Whitelist?
=================================================================

If you run commands related to normal services on the server, HSS generates high-risk command execution alarms. You can add a whitelist to prevent the alarm.

To add a command alarm whitelist, perform the following steps:

#. Log in to the management console.
#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.
#. In the navigation pane, choose **Security Operations** > **Policies**.
#. Locate the policy group of the protected edition corresponding to the server and click the policy group name.
#. Click **Real-time Process**.
#. Add a command whitelist. The parameters are as follows:

   -  Full path or program name of a process: Enter the full path or program name of the process, for example, **/usr/bin/sleep** or **sleep**.
   -  Regular expression in CLI: Enter the regular expression of the command to be added to the whitelist, for example, **^[A-Za-z0-9[:space:]\\\\*\\\\.\\\\\\":_'\\\\(>=-]+$**.

#. Click **OK** to save the change.

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png

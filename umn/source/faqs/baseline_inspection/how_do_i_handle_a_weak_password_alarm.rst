:original_name: hss_01_0197.html

.. _hss_01_0197:

How Do I Handle a Weak Password Alarm?
======================================

Servers using weak passwords are exposed to intrusions. If a weak password alarm is reported, you are advised to change the alarmed password immediately.

Causes
------

-  If simple passwords are used and match those in the weak password library, a weak password alarm will be generated.
-  A password used by multiple member accounts will be regarded as a weak password and trigger an alarm.

Checking and Changing Weak Passwords
------------------------------------

#. Log in to the management console.
#. Choose **Prediction** > **Baseline Checks** and click the **Common Weak Password Detection** tab.
#. Check the server, account name, account type, and usage duration of the weak password. Log in to the server and change the password.

Changing a Weak Password
------------------------

+-----------------------+---------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------+
| System                | Procedure                                                                             | Remarks                                                                                |
+=======================+=======================================================================================+========================================================================================+
| Windows OS            | To change the password in the Windows 10, perform the following steps:                | None                                                                                   |
|                       |                                                                                       |                                                                                        |
|                       | #. Log in to the Windows OS.                                                          |                                                                                        |
|                       | #. Click |image1| in the lower left corner and click |image2|.                        |                                                                                        |
|                       | #. In the **Windows Settings** window, click **Accounts**.                            |                                                                                        |
|                       | #. Choose **Sign-in options** from the navigation tree.                               |                                                                                        |
|                       | #. On the **Sign-in options** tab, click **Change** under **Password**.               |                                                                                        |
+-----------------------+---------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------+
| Linux OS              | Log in to the Linux server and run the following command:                             | If you do not specify any username, you are changing the password of the current user. |
|                       |                                                                                       |                                                                                        |
|                       | **passwd [<user>]**                                                                   | After the command is executed, enter the new password as prompted.                     |
|                       |                                                                                       |                                                                                        |
|                       |                                                                                       | .. note::                                                                              |
|                       |                                                                                       |                                                                                        |
|                       |                                                                                       |    Replace *<user>* with the username.                                                 |
+-----------------------+---------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------+
| MySQL database        | #. Log in to the MySQL database.                                                      | None                                                                                   |
|                       |                                                                                       |                                                                                        |
|                       | #. Run the following command to check the database user password:                     |                                                                                        |
|                       |                                                                                       |                                                                                        |
|                       |    **SELECT user, host, authentication_string From user;**                            |                                                                                        |
|                       |                                                                                       |                                                                                        |
|                       |    This command is probably invalid in certain MySQL versions.                        |                                                                                        |
|                       |                                                                                       |                                                                                        |
|                       |    In this case, run the following command:                                           |                                                                                        |
|                       |                                                                                       |                                                                                        |
|                       |    **SELECT user, host password From user;**                                          |                                                                                        |
|                       |                                                                                       |                                                                                        |
|                       | #. Run the following command to change the password:                                  |                                                                                        |
|                       |                                                                                       |                                                                                        |
|                       |    **SET PASSWORD FOR'Username'@'Host'=PASSWORD('New_password');**                    |                                                                                        |
|                       |                                                                                       |                                                                                        |
|                       | #. Run the following command to refresh password settings:                            |                                                                                        |
|                       |                                                                                       |                                                                                        |
|                       |    **flush privileges;**                                                              |                                                                                        |
+-----------------------+---------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------+
| Redis database        | #. Open the Redis database configuration file **redis.conf**.                         | -  If there is already a password, the command will change it to the new password.     |
|                       |                                                                                       | -  If there has been no password set, the command will set the password.               |
|                       | #. Run the following command to change the password:                                  |                                                                                        |
|                       |                                                                                       | .. note::                                                                              |
|                       |    **requirepass <password>;**                                                        |                                                                                        |
|                       |                                                                                       |    Replace *<password>* with the new password.                                         |
+-----------------------+---------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------+
| Tomcat                | #. Open the **conf/tomcat-user.xml** configuration file in the Tomcat root directory. | None                                                                                   |
|                       | #. Change the value of **password** under the **user** node to a strong password.     |                                                                                        |
+-----------------------+---------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------+

.. |image1| image:: /_static/images/en-us_image_0000001517477582.png
.. |image2| image:: /_static/images/en-us_image_0000001568317737.png

:original_name: hss_01_0014.html

.. _hss_01_0014:

What Can I Do If I Enabled Dynamic WTP But Its Status Is Enabled but not in effect?
===================================================================================

Dynamic WTP protects your Tomcat applications.

For this function to take effect, ensure that:

-  There are Tomcat applications running on your servers.
-  Your servers run the Linux OS.
-  The **setenv.sh** file has been automatically generated in the **tomcat/bin** directory (usually 20 minutes after you enable dynamic WTP). If the file exists, restart Tomcat to make dynamic WTP take effect.

If the status of dynamic WTP is **Enabled but not in effect** after you enable it, perform the following operations:

-  Check whether the **setenv.sh** file has been generated in the **tomcat/bin** directory.
-  If the **setenv.sh** file exists, check whether Tomcat has been restarted.

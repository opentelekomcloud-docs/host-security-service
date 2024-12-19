:original_name: hss_01_0483.html

.. _hss_01_0483:

Uninstalling a Plug-in
======================

Uninstall the Docker plug-in if you do not need to use the image blocking function.

Uninstalling a Docker Plug-in
-----------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane on the left, choose **Installation & Configuration** > **Plug-in Settings**. Click **Plug-In Uninstallation Guide**. In the slide-out panel, copy the commands in the **Uninstallation Commands** section.


   .. figure:: /_static/images/en-us_image_0000001622047062.png
      :alt: **Figure 1** Obtaining the Docker plug-in uninstallation command

      **Figure 1** Obtaining the Docker plug-in uninstallation command

#. Remotely log in to the server where the plug-in is to be uninstalled as the **root** user.

   -  If your server has an EIP bound, you can also use a remote management tool, such as PuTTY or Xshell, to log in to the server and uninstall the plug-in on the server as user **root**.

#. Run the following command to access the **/tmp** directory:

   .. code-block::

      cd /tmp/

#. Create **linux-host-list.txt**, which will contain the server private IP addresses where the plug-in is to be uninstalled:

   Command syntax:

   .. code-block::

      echo 127.8.8.8 22 root rootPassword >> linux-host-list.txt

   .. code-block::

      Or echo 127.8.8.8 22 user userPassword rootPassword >> linux-host-list.txt

   To specify multiple IP addresses, write multiple commands, each in a separate line.

   Example:

   .. code-block::

      echo 127.8.8.1 22 root rootPassword >> linux-host-list.txt
      echo 127.8.8.2 22 user userPassword rootPassword >> linux-host-list.txt
      echo 127.8.8.3 22 root rootPassword >> linux-host-list.txt

#. Press **Enter** to save the IP address. Run the **cat linux-host-list.txt** command to verify the IP addresses have been added.

#. Copy the batch uninstallation commands to the command box and press **Enter**. The uninstallation starts automatically.

#. If **remote_uninstall finished. [OK]** is displayed, the uninstallation is successful. Wait for 3 to 5 minutes and check the Docker plug-in status of the panel server.

   |image2|

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png
.. |image2| image:: /_static/images/en-us_image_0000001568637413.png

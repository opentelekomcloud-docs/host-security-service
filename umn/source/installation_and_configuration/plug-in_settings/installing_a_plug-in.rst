:original_name: hss_01_0481.html

.. _hss_01_0481:

Installing a Plug-in
====================

If container protection is enabled and you want to use the image blocking function, install the Docker plug-in by following the instructions provided in this section.


Installing a Plug-in
--------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner of the page, select a region, and choose **Security** > **Host Security Service**. The HSS page is displayed.

#. In the navigation pane on the left, choose **Installation & Configuration** > **Plug-in Settings**. Click **Plug-In Installation Guide**. In the slide-out panel, copy the commands in the **Installation Commands** section.


   .. figure:: /_static/images/en-us_image_0000001670646697.png
      :alt: **Figure 1** Obtaining the Docker plug-in installation command

      **Figure 1** Obtaining the Docker plug-in installation command

#. Remotely log in to the server where the plug-in is to be installed as the **root** user.

   -  If your server has an EIP bound, you can also use a remote management tool, such as PuTTY or Xshell, to log in to the server and install the plug-in on the server as user **root**.

#. Run the following command to access the **/tmp** directory:

   .. code-block::

      cd /tmp/

#. Create **linux-host-list.txt**, which will contain the server private IP addresses where the agent is to be installed:

   Command syntax:

   .. code-block::

      echo 127.8.8.8 22 root rootPassword >> linux-host-list.txt

   .. code-block::

      Or
      echo 127.8.8.8 22 user userPassword rootPassword >> linux-host-list.txt

   To specify multiple IP addresses, write multiple commands, each in a separate line.

   Example:

   .. code-block::

      echo 127.8.8.1 22 root rootPassword >> linux-host-list.txt
      echo 127.8.8.2 22 user userPassword rootPassword >> linux-host-list.txt
      echo 127.8.8.3 22 root rootPassword >> linux-host-list.txt

#. Press **Enter** to save the IP address. Run the **cat linux-host-list.txt** command to verify the IP addresses have been added.

#. Copy the batch installation commands to the command terminal and press **Enter**.

#. If **remote_install finished. [OK]** is displayed, the installation is successful. Wait for 3 to 5 minutes and check the Docker plug-in status of the panel server.

   |image2|

.. |image1| image:: /_static/images/en-us_image_0000001517477398.png
.. |image2| image:: /_static/images/en-us_image_0000001517637682.png

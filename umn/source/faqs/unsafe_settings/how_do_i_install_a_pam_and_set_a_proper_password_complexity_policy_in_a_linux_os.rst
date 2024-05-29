:original_name: hss_01_0043.html

.. _hss_01_0043:

How Do I Install a PAM and Set a Proper Password Complexity Policy in a Linux OS?
=================================================================================

Installing a PAM
----------------

Your password complexity policy cannot be checked if no pluggable authentication module (PAM) is running in your system.

For Debian or Ubuntu, run the **apt-get install libpam-cracklib** command as the administrator to install a PAM.

.. note::

   A PAM is installed and running by default in CentOS, Fedora, and EulerOS.

Setting a Password Complexity Policy
------------------------------------

A proper password complexity policy would be: the password must contain at least eight characters and must contain uppercase letters, lowercase letters, numbers, and special characters.

.. note::

   The preceding configurations are basic security requirements. For more security configurations, run the following commands to obtain help information in Linux OSs:

   -  For CentOS, Fedora, and EulerOS based on Red Hat 7.0, run:

      **man pam_pwquality**

   -  For other Linux OSs, run:

      **man pam_cracklib**

-  CentOS, Fedora, and EulerOS

   #. Run the following command to edit the **/etc/pam.d/system-auth** file:

      **vi** **/etc/pam.d/system-auth**

   #. Find the following information in the file:

      -  For CentOS, Fedora, and EulerOS based on Red Hat 7.0:

         password requisite pam_pwquality.so try_first_pass retry=3 type=

      -  For other CentOS, Fedora, and EulerOS systems:

         password requisite pam_cracklib.so try_first_pass retry=3 type=

   #. Add the following parameters and their values: **minlen**, **dcredit**, **ucredit**, **lcredit**, and **ocredit**. If the file already has these parameters, change their values. For details, see :ref:`Table 1 <hss_01_0043__table55305016336>`.

      Example:

      password requisite pam_cracklib.so try_first_pass retry=3 minlen=8 dcredit=-1 ucredit=-1 lcredit=-1 ocredit=-1 type=

      .. note::

         Set **dcredit**, **ucredit**, **lcredit**, and **ocredit** to negative numbers.

      .. _hss_01_0043__table55305016336:

      .. table:: **Table 1** Parameter description

         +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
         | Parameter             | Description                                                                                                                                                                   | Example               |
         +=======================+===============================================================================================================================================================================+=======================+
         | minlen                | Minimum length of a password.                                                                                                                                                 | minlen=8              |
         |                       |                                                                                                                                                                               |                       |
         |                       | For example, if you want the minimum length to be eight, set the **minlen** value to 8.                                                                                       |                       |
         +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
         | dcredit               | Number of digits                                                                                                                                                              | dcredit=-1            |
         |                       |                                                                                                                                                                               |                       |
         |                       | A negative value (for example, **-N**) indicates the number (for example, N) of digits required in a password. A positive value indicates that there is no limit.             |                       |
         +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
         | ucredit               | Number of uppercase letters                                                                                                                                                   | ucredit=-1            |
         |                       |                                                                                                                                                                               |                       |
         |                       | A negative value (for example, **-N**) indicates the number (for example, N) of uppercase letters required in a password. A positive value indicates that there is no limit.  |                       |
         +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
         | lcredit               | Number of lowercase letters                                                                                                                                                   | lcredit=-1            |
         |                       |                                                                                                                                                                               |                       |
         |                       | A negative value (for example, **-N**) indicates the number (for example, N) of lowercase letters required in a password. A positive value indicates that there is no limit.  |                       |
         +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
         | ocredit               | Number of special characters                                                                                                                                                  | ocredit=-1            |
         |                       |                                                                                                                                                                               |                       |
         |                       | A negative value (for example, **-N**) indicates the number (for example, N) of special characters required in a password. A positive value indicates that there is no limit. |                       |
         +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+

-  Debian and Ubuntu

   #. Run the following command to edit the **/etc/pam.d/common-password** file:

      **vi /etc/pam.d/common-password**

   #. Find the following information in the file:

      password requisite pam_cracklib.so retry=3 minlen=8 difok=3

   #. Add the following parameters and their values: **minlen**, **dcredit**, **ucredit**, **lcredit**, and **ocredit**. If the file already has these parameters, change their values. For details, see :ref:`Table 1 <hss_01_0043__table55305016336>`.

      Example:

      password requisite pam_cracklib.so retry=3 minlen=8 dcredit=-1 ucredit=-1 lcredit=-1 ocredit=-1 difok=3

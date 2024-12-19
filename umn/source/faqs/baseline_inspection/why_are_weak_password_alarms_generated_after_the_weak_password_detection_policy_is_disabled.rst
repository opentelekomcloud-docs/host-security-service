:original_name: hss_01_0274.html

.. _hss_01_0274:

Why Are Weak Password Alarms Generated After the Weak Password Detection Policy Is Disabled?
============================================================================================

If you have enhanced passwords before disabling the weak password policy, the weak password alarm will not be reported again.

If you do not enhance passwords before disabling the weak password policy, the reported alarm will persist and be retained for 30 days.

-  To enhance server security, you are advised to modify the accounts with weak passwords in a timely manner, such as SSH accounts.
-  To protect internal data of your server, you are advised to modify software accounts that use weak passwords, such as MySQL accounts and FTP accounts.

After modifying weak passwords, you are advised to perform manual detection immediately to verify the result. If you do not perform manual verification and do not disable the weak password scan, HSS will automatically check the settings the next day in the early morning.

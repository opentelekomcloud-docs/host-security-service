:original_name: hss_01_0004.html

.. _hss_01_0004:

Basic Concepts
==============

Account Cracking
----------------

Account cracking refers to the intruder behavior of guessing or cracking the password of an account.

Baseline
--------

A baseline specifies the minimum security configuration requirements that the OS and database configurations must meet in terms of account management, password policy configuration, authorization management, service management, configuration management, network configuration, and permission management. HSS provides the cloud security practice baseline and the general security standard baseline detection to meet diverse security compliance requirements.

Weak Password
-------------

A weak password can be easily cracked.

Malicious Program
-----------------

A malicious program, such as a web shell, Trojan, worm, or virus, is developed with attack or illegal remote control intents.

Malware covertly inlays code into another program to run intrusive or disruptive programs and damage the security and integrity of the data on an infected server. Malware includes viruses, Trojans, and worms, classified by their ways of transmission.

HSS reports both identified and suspicious malware.

Ransomware
----------

Ransomware emerged with the Bitcoin economy. It is a Trojan that is disguised as a legitimate email attachment or bundled software and tricks you into opening or installing it. It can also arrive on your servers through website or server intrusion.

Ransomware often uses a range of algorithms to encrypt the victim's files and demand a ransom payment to get the decryption key. Digital currencies such as Bitcoin are typically used for the ransoms, making tracing and prosecuting the attackers difficult.

Ransomware interrupts businesses and can cause serious economic losses. We need to know how it works and how we can prevent it.

Two-Factor Authentication
-------------------------

Two-factor authentication (2FA) refers to the authentication of user login by the combination of the user password and a verification code.

Web Tamper Protection
---------------------

Web Tamper Protection (WTP) is an HSS edition that protects your files, such as web pages, documents, and images, in specific directories against tampering and sabotage from hackers and viruses.

Cluster
-------

A cluster consists of one or more ECSs (also known as nodes) in the same subnet. It provides a computing resource pool for running containers.

Node
----

In CGS, each node corresponds to an ECS. Containers run on nodes.

Image
-----

An image is a special file system. It provides not only programs, libraries, resources, configuration files but also some configuration parameters required for a running container. A Docker image does not contain any dynamic data, and its content remains unchanged after being built.

Container
---------

A container is the instance of an image and can be created, started, stopped, deleted, and suspended.

Container Runtime
-----------------

Container runtime, one of the most important components of Kubernetes, manages the lifecycle of images and containers. kubelet interacts with a container runtime through the Container Runtime Interface (CRI) to manage images and containers.

Security Policy
---------------

A security policy indicates the security rule that must be followed for a running container. If a container violates a security policy, a container exception is displayed on the **Runtime Security** page of the CGS management console.

Project
-------

Projects are used to group and isolate OpenStack resources, including computing, storage, and network resources. A project can be a department or a project team.

Multiple projects can be created for one account.

Protection Quota
----------------

To protect a server, bind it to an HSS quota.

The quotas of different HSS editions you applied for are displayed on the console.

Example:

-  If you have applied for an HSS enterprise edition quota, you can bind it to a server.
-  If you have applied for 10 HSS enterprise edition quotas, you can bind them to 10 servers.

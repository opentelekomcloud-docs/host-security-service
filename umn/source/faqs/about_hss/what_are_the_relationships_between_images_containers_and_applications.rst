:original_name: hss_01_0320.html

.. _hss_01_0320:

What Are the Relationships Between Images, Containers, and Applications?
========================================================================

-  An image is a special file system. It provides programs, libraries, resources, configuration files and other files required for a running container. An image also contains some configuration parameters (such as anonymous volumes, environment variables, and users) prepared for a running container. An image does not contain any dynamic data, and its content is unchangeable after creation.
-  The relationship between the image and container is similar to that between the class and instance in the program design. An image is static, and a container is the entity for a running image. A container can be created, started, stopped, deleted, and suspended.
-  Multiple containers can be started for an image.
-  An application may include one or a set of containers.

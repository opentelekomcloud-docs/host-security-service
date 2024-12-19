:original_name: hss_01_0549.html

.. _hss_01_0549:

What Do I Do If the Container Cluster Protection Plug-in Fails to Be Uninstalled?
=================================================================================

Possible Causes
---------------

If the cluster network is abnormal or the plug-in is running, uninstalling the plug-in on the HSS console may fail.

Solution
--------

Perform the following operations on any cluster node to uninstall the container cluster protection plug-in:

#. Log in to a cluster node.

#. Create the file **plugin.yaml** in the **/tmp** directory and copy the following script content to the file:

   .. code-block::

      apiVersion: v1
      kind: Namespace
      metadata:
        labels:
          admission.gatekeeper.sh/ignore: no-self-managing
          control-plane: controller-manager
          gatekeeper.sh/system: "yes"
          pod-security.kubernetes.io/audit: restricted
          pod-security.kubernetes.io/audit-version: latest
          pod-security.kubernetes.io/enforce: restricted
          pod-security.kubernetes.io/enforce-version: v1.24
          pod-security.kubernetes.io/warn: restricted
          pod-security.kubernetes.io/warn-version: latest
        name: gatekeeper-system
      ---
      apiVersion: apiextensions.k8s.io/v1
      kind: CustomResourceDefinition
      metadata:
        annotations:
          controller-gen.kubebuilder.io/version: v0.10.0
        labels:
          gatekeeper.sh/system: "yes"
        name: assign.mutations.gatekeeper.sh
      ---
      apiVersion: apiextensions.k8s.io/v1
      kind: CustomResourceDefinition
      metadata:
        annotations:
          controller-gen.kubebuilder.io/version: v0.10.0
        labels:
          gatekeeper.sh/system: "yes"
        name: assignimage.mutations.gatekeeper.sh
      ---
      apiVersion: apiextensions.k8s.io/v1
      kind: CustomResourceDefinition
      metadata:
        annotations:
          controller-gen.kubebuilder.io/version: v0.10.0
        labels:
          gatekeeper.sh/system: "yes"
        name: assignmetadata.mutations.gatekeeper.sh
      ---
      apiVersion: apiextensions.k8s.io/v1
      kind: CustomResourceDefinition
      metadata:
        annotations:
          controller-gen.kubebuilder.io/version: v0.10.0
        labels:
          gatekeeper.sh/system: "yes"
        name: configs.config.gatekeeper.sh
      ---
      apiVersion: apiextensions.k8s.io/v1
      kind: CustomResourceDefinition
      metadata:
        annotations:
          controller-gen.kubebuilder.io/version: v0.10.0
        labels:
          gatekeeper.sh/system: "yes"
        name: constraintpodstatuses.status.gatekeeper.sh
      ---
      apiVersion: apiextensions.k8s.io/v1
      kind: CustomResourceDefinition
      metadata:
        annotations:
          controller-gen.kubebuilder.io/version: v0.10.0
        labels:
          gatekeeper.sh/system: "yes"
        name: constrainttemplatepodstatuses.status.gatekeeper.sh
      ---
      apiVersion: apiextensions.k8s.io/v1
      kind: CustomResourceDefinition
      metadata:
        annotations:
          controller-gen.kubebuilder.io/version: v0.11.3
        labels:
          gatekeeper.sh/system: "yes"
        name: constrainttemplates.templates.gatekeeper.sh
      ---
      apiVersion: apiextensions.k8s.io/v1
      kind: CustomResourceDefinition
      metadata:
        annotations:
          controller-gen.kubebuilder.io/version: v0.10.0
        labels:
          gatekeeper.sh/system: "yes"
        name: expansiontemplate.expansion.gatekeeper.sh
      ---
      apiVersion: apiextensions.k8s.io/v1
      kind: CustomResourceDefinition
      metadata:
        annotations:
          controller-gen.kubebuilder.io/version: v0.10.0
        labels:
          gatekeeper.sh/system: "yes"
        name: expansiontemplatepodstatuses.status.gatekeeper.sh
      ---
      apiVersion: apiextensions.k8s.io/v1
      kind: CustomResourceDefinition
      metadata:
        annotations:
          controller-gen.kubebuilder.io/version: v0.10.0
        labels:
          gatekeeper.sh/system: "yes"
        name: modifyset.mutations.gatekeeper.sh
      ---
      apiVersion: apiextensions.k8s.io/v1
      kind: CustomResourceDefinition
      metadata:
        annotations:
          controller-gen.kubebuilder.io/version: v0.10.0
        labels:
          gatekeeper.sh/system: "yes"
        name: mutatorpodstatuses.status.gatekeeper.sh
      ---
      apiVersion: apiextensions.k8s.io/v1
      kind: CustomResourceDefinition
      metadata:
        annotations:
          controller-gen.kubebuilder.io/version: v0.11.3
        labels:
          gatekeeper.sh/system: "yes"
        name: providers.externaldata.gatekeeper.sh
      ---
      apiVersion: rbac.authorization.k8s.io/v1
      kind: Role
      metadata:
        creationTimestamp: null
        labels:
          gatekeeper.sh/system: "yes"
        name: gatekeeper-manager-role
        namespace: gatekeeper-system
      ---
      apiVersion: rbac.authorization.k8s.io/v1
      kind: ClusterRole
      metadata:
        creationTimestamp: null
        labels:
          gatekeeper.sh/system: "yes"
        name: gatekeeper-manager-role
      ---
      apiVersion: rbac.authorization.k8s.io/v1
      kind: RoleBinding
      metadata:
        labels:
          gatekeeper.sh/system: "yes"
        name: gatekeeper-manager-rolebinding
        namespace: gatekeeper-system
      roleRef:
        apiGroup: rbac.authorization.k8s.io
        kind: Role
        name: gatekeeper-manager-role
      subjects:
      - kind: ServiceAccount
        name: gatekeeper-admin
        namespace: gatekeeper-system
      ---
      apiVersion: rbac.authorization.k8s.io/v1
      kind: ClusterRoleBinding
      metadata:
        labels:
          gatekeeper.sh/system: "yes"
        name: gatekeeper-manager-rolebinding
      roleRef:
        apiGroup: rbac.authorization.k8s.io
        kind: ClusterRole
        name: gatekeeper-manager-role
      subjects:
      - kind: ServiceAccount
        name: gatekeeper-admin
        namespace: gatekeeper-system
      ---
      apiVersion: admissionregistration.k8s.io/v1
      kind: MutatingWebhookConfiguration
      metadata:
        labels:
          gatekeeper.sh/system: "yes"
        name: gatekeeper-mutating-webhook-configuration
      ---
      apiVersion: admissionregistration.k8s.io/v1
      kind: ValidatingWebhookConfiguration
      metadata:
        labels:
          gatekeeper.sh/system: "yes"
        name: gatekeeper-validating-webhook-configuration

3. Create the file **uninstall.sh** in the **/tmp** directory and copy the following script content to the file:

   .. code-block::

      #!/bin/bash
      kubectl delete -f /tmp/plugin.yaml
      kubectl delete ns cgs-provider

4. Run the following command to uninstall the container cluster protection plug-in:

   .. code-block::

      bash /tmp/uninstall.sh

   If information similar to the following is displayed, the plug-in has been uninstalled.

   |image1|

.. |image1| image:: /_static/images/en-us_image_0000001673926668.png

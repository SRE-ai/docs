---
description: >-
  Learn how to configure and manage instances for different environments in
  SRE.ai.
---

# Instances

Instances allow you to create connections to your Salesforce environments and assign them a specific purpose, such as:

* Development
* Code integration
* Quality analysis
* User testing
* Production

The Instance's name may or may not match the name of the associated sandbox.

Instances allow you to update the connected sandbox environment over time while keeping your work tied to the Instance.

You can connect to your Salesforce environments in three ways:

* DX Orgs (recommended)
* OAuth
* Username and password

<figure><img src="../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

An Instance can be associated with a git branch, allowing you to commit and promote (merge and deploy) changes while managing git workflows in the background.

You can also set a parent Instance to create a deployment pipeline and use the environment strategy of your choice.

<figure><img src="../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

Quality controls, such as code review requirements, test class execution, and deployment options, can be set at the Instance level and enforced during promotion and deployment.\


<figure><img src="../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

With workspace, you can control who within your team can do the following to an Instance:

* Access
* Commit
* Promote
* Deploy
* Manage

---
description: Learn how to set up SRE.ai.
icon: flag-checkered
---

# Getting Started

To get started, download and install the latest .dmg (for Mac) or .exe (for Windows) from [the releases](https://github.com/support-infinit/infinit-desktop/releases).

Log in with your email address to receive a secured token via email.

Each login requires this token, and the application will stay connected until you log out.

The "LOCAL (offline)" workspace is available by default and is a good starting point for evaluating the platform.

The LOCAL workspace gives you access to all the features of SRE.ai for individual use, except for collaboration, which requires [creating or being invited to a workspace.](quickstart.md#setting-up-workspace)

{% hint style="info" %}
I**MPORTANT:** [Git](https://git-scm.com/downloads) must be pre-installed for all functions to work correctly.
{% endhint %}

***

## Setting up workspace

Learn about the basics of a workspace, and how to install SRE.ai into the workspace.

### Workspace basics

A workspace is a collaborative space where team members can work together. As an administrator, you can control each team member's permissions by turning certain access rights on or off.

To invite team members to the workspace, add their email addresses as members.

{% hint style="info" %}
You must have the **Manage Workspace** permission as the administrator to perform these tasks.
{% endhint %}

<figure><img src=".gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

To use the workspace, connect to a Salesforce environment with the SRE.ai packages installed. The Salesforce environment connected to the workspace is a remote connection for storing and synchronizing data from SRE.ai with other team members.\
\
Each team member must connect to the remote Salesforce environment using their credentials.

<figure><img src=".gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

### Setting up SRE.ai in the workspace

The SRE.ai package for Salesforce is an AppExchange-managed Package. Use [the provided installation link](https://login.salesforce.com/packaging/installPackage.apexp?p0=04tHr000001WlGqIAK) to install the SRE.ai package for Salesforce.\
\
After installation, assign the **SRE.ai User** permission set to SRE.ai users to grant them access to SRE.ai objects, classes, and other components.


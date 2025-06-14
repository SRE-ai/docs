---
description: Learn about the customizable parameters in each Step
---

# Steps customization

## Overview

SRE.ai offers eighteen step types:

* [Create Change](steps-customization.md#create-change-step-customization)
* [Create Collection](steps-customization.md#create-collection-step-customization)
* [Add to Collection](steps-customization.md#add-collection-step-customization)
* [Remove from Collection](steps-customization.md#remove-from-collection-step-customization)
* [Import Changes](steps-customization.md#import-changes-step-customization)
* [Commit](steps-customization.md#commit-step-customization)
* [Promote](steps-customization.md#promote-step-customization)
* [Deploy](steps-customization.md#deploy-step-customization)
* [Install Package](steps-customization.md#install-package-step-customization)
* [Create Package Version](steps-customization.md#create-package-version-step-customization)
* [Create Scratch Org](steps-customization.md#create-scratch-org-step-customization)
* [Update Jira Issue](steps-customization.md#update-jira-issue-step-customization)
* [Create Pull Request](steps-customization.md#create-pull-request-step-customization)
* [Review Pull Request](steps-customization.md#review-pull-request-step-customization)
* [Pull Request Exception](steps-customization.md#pull-request-exception-step-customization)
* [Summarize Change](steps-customization.md#summarize-change-step-customization)
* [List Components](steps-customization.md#list-components-step-customization)
* [Post a Slack Message](steps-customization.md#post-slack-message-step-customization)

Read below to learn about the parameters that can be customized within each step.

## Create Change step customization

The Create Change step features three customizable parameters:

* **Name**
* **Description**
* **Source Instance (**_**required**_**)**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 5.02.01 PM.png" alt="" width="375"><figcaption></figcaption></figure>

The available **Source Instances** depend on the Salesforce environment you are connected to.

## Create Collection step customization

The Create Change step features three customizable parameters:

* **Name**
* **Description**
* **Source Instance (**_**required**_**)**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 5.07.30 PM.png" alt="" width="375"><figcaption></figcaption></figure>

The available **Source Instances** depend on the Salesforce environment you are connected to.

## Add to Collection step customization

The Add to Collection step features two customizable parameters:

* **Name**
* **Description**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 5.08.46 PM.png" alt="" width="375"><figcaption></figcaption></figure>

## Remove from Collection step customization

The Remove from Collection step features two customizable parameters:

* **Name**
* **Description**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 5.10.09 PM.png" alt="" width="375"><figcaption></figcaption></figure>

## Import Changes step customization

<details>

<summary><mark style="background-color:yellow;">Click to learn more about the Import Changes step</mark></summary>

The Import Changes step features six customizable parameters:

* **Name**
* **Description**
* **Select Change (**_**optional**_**)**
* **Select Source Instance (**_**optional**_**)**
* **Changes filter**
* **Time range filter**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 5.12.58 PM.png" alt="" width="375"><figcaption></figcaption></figure>

The environment you connect to impacts the elements within the **Select Change** and **Select Source Instance** parameters.

The **Changes filter** parameter features two options:

* **My changes** - show only components you have changed
* **All changes** - show all components that have changed

The **Time range filter** parameter features six options:

* **Today**
* **Yesterday**
* **This week**
* **Last week**
* **This month**
* **Last 90 days**

</details>

***

## Commit step customization

The Commit step features five customizable parameters:

* **Name**
* **Description**
* **Select change (**_**optional**_**)**
* **Select Source Instance (**_**optional**_**)**
* **Select Repository (**_**optional**_**)**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 5.29.06 PM.png" alt="" width="375"><figcaption></figcaption></figure>

The environment you connect to impacts the elements within the **Select Change**, **Select Source Instance**, and **Select Repository** parameters.

## Promote step customization

<details>

<summary><mark style="background-color:yellow;"><strong>Click to learn more about the Promote step</strong></mark></summary>

The Promote step features nine customizable parameters:

* **Name**
* **Description**
* **Select Target Instance (**_**required**_**)**
* **Type**
* **Select Change (**_**optional**_**)**
* **Conflict resolution**
* **Check only** option - run a validation check without making any changes to the target org
* **Close branch** option - delete the branch after the merge is successful
* **Back promote** option - check when promoting down in the release chain

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 6.05.48 PM.png" alt="" width="375"><figcaption></figcaption></figure>

The environment you connect to impacts the elements within the **Select Target Instance** and **Select Change** parameters.

The **Conflict resolution** parameter offers four options:

* Auto-resolve (when possible)
* Resolve manually
* Favor source branch
* Favor target branch

</details>

## Deploy step customization

The Deploy step features seven customizable parameters:

* **Name**
* **Description**
* **Select Target Instance (**_**optional**_**)**
* **Type**
* **Select Collection (**_**required**_**)**
* **Select Source (**_**required**_**)**
* **Check only** option - run a validation check without making any changes to the target org

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 6.19.19 PM.png" alt="" width="375"><figcaption></figcaption></figure>

The environment you connect to impacts the elements within the **Select Target Instance**, **Select Collection**, and **Select Source** parameters.

## Install Package step customization

<details>

<summary><mark style="background-color:yellow;"><strong>Click to learn more about the Install Package step</strong></mark></summary>

The Install Package step features nine customizable parameters:

* **Name**
* **Description**
* **Select Target Instance (**_**optional**_**)**
* **Select DevHub Instance (**_**required**_**)**
* **Package Options**
* **Installation key**
* **Package access type**
* **Upgrade type**
* **Apex compile option**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 6.21.28 PM.png" alt="" width="375"><figcaption></figcaption></figure>

The environment you connect to impacts the elements within the **Select Target Instance** and **Select DevHub Instance** parameters.

</details>

## Create Package Version step customization

<details>

<summary><mark style="background-color:yellow;"><strong>Click to learn more about the Create Package Version step</strong></mark></summary>

The Create Package step features five main customizable parameters:

* **Name**
* **Description**
* **Select DevHub Instance (**_**required**_**)**
* **Source branch (**_**required**_**)**
* **Installation key**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 7.09.26 PM.png" alt="" width="375"><figcaption></figcaption></figure>

The environment you connect to impacts the elements within the **Select Target Instance** and **Select DevHub Instance** parameters.

### Hidden parameters

The Create Package Version step also features ten customizable parameters that are hidden by default:

* **Definition file**
* **Tag**
* **Skip Validation** option - don't include second-generation managed package (2GP) ancestors
* **Code Coverage** option - calculate and store the code coverage percentage by running the packaged Apex tests included in this package version
* **Skip Ancestor Check** option - overrides ancestry requirements, which allows you to specify a packaged ancestor that isn't the highest released package version
* **Post-Install Script**
* **Uninstall Script**
* **Post Install URL**
* **Release Notes URL**
* **Language**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 7.10.20 PM.png" alt="" width="375"><figcaption></figcaption></figure>

</details>

## Create Scratch Org step customization

<details>

<summary><mark style="background-color:yellow;"><strong>Click to learn more about the Create Scratch Org step</strong></mark></summary>

The Create Scratch Org step features five main customizable parameters:

* **Name**
* **Description**
* **Select DevHub Instance (**_**required**_**)**
* **Duration days**

{% hint style="info" %}
**NOTE:** The default value for **Duration days** is 7. The upper limit is 30.
{% endhint %}

* **Edition**
* **Options**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 7.22.31 PM.png" alt="" width="375"><figcaption></figcaption></figure>

The environment you connect to impacts the elements within the **Select DevHub Instance** parameter.

### Edition parameter options

The **Edition** parameter offers eight options:

* Developer
* Enterprise
* Group
* Professional
* Partner Developer
* Partner Enterprise
*

    <figure><img src="../../.gitbook/assets/Screenshot 2025-04-25 at 10.35.55 AM.png" alt="" width="375"><figcaption></figcaption></figure>
* Partner Group
* Partner Professional

### Hidden parameters

The Create Scratch Org  step also features six customizable parameters that are hidden by default:

* **Org Name**
* **Description**
* **Release**&#x20;
* **No Ancestors** option - don't include second generation managed package (2GP) ancestors
* **No Namespace** option - create the scratch org with no namespace, even if the DevHub has a namespace
* **No Source Tracking** option - disables source tracking in the new scratch org

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 7.43.43 PM.png" alt="" width="375"><figcaption></figcaption></figure>

</details>

## Update Jira Issue step customization

The Update Jira Issue step features three main customizable parameters:

* **Name**
* **Description**
* **Select Connection (**_**required**_**)**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-25 at 10.32.46 AM.png" alt="" width="375"><figcaption></figcaption></figure>

## Create Pull Request step customization

The Create Pull Request step features four main customizable parameters:

* **Name**
* **Description**
* **Select Connection (**_**required**_**)**
* **Destination branch**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-28 at 7.00.12 PM.png" alt="" width="362"><figcaption></figcaption></figure>

## Review Pull Request step customization

<details>

<summary><mark style="background-color:yellow;"><strong>Click to learn more about the Review Pull Request step</strong></mark></summary>

The Review Pull Request step features seven main customizable parameters:

* **Name**
* **Description**
* **Select Connection (**_**required**_**)**
* **Destination branch**
* **Complexity Threshold**
* **AI Model**
* **Additional Instructions**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-25 at 10.37.59 AM.png" alt="" width="375"><figcaption></figcaption></figure>

### AI Model options

The AI Model parameter offers six options:

* SRE.ai Salesforce 1.0
* Claude 3.5 Sonnet
* Gemini 2.0 Flash
* GPT 4o
* o1
* o3-mini

</details>

## Pull Request Exception step customization

The Pull Request Exception step features eight main customizable parameters:

* **Name**
* **Description**
* **Select Connection (**_**required**_**)**
* **Destination branch**
* **Pull Request Label**
* **Auto Approve** toggle
* **Criteria**
* **Types**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-25 at 11.02.22 AM.png" alt="" width="375"><figcaption></figcaption></figure>

## Summarize Change step customization

The List Components step features three main customizable parameters:

* **Name**
* **Description**
* **Select Connection (**_**required**_**)**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-25 at 1.44.58 PM.png" alt="" width="375"><figcaption></figcaption></figure>

## List Components step customization

The List Components step features three main customizable parameters:

* **Name**
* **Description**
* **Select Connection (**_**required**_**)**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-25 at 1.44.58 PM.png" alt="" width="375"><figcaption></figcaption></figure>

## Post Slack Message step customization

The Post Slack Message step features three main customizable parameters:

* **Name**
* **Description**
* **Select Connection (**_**required**_**)**
* **Channel (**_**required**_**)**
* **Message**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-25 at 1.49.40 PM.png" alt="" width="375"><figcaption></figcaption></figure>


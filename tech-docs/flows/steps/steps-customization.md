---
description: Learn about the customizable parameters in each Step
---

# Steps customization

## Overview

SRE.ai offers eighteen Step types:

* Create Change
* Create Collection
* Add to Collection
* Remove from Collection
* Import Changes
* Commit
* Promote
* Deploy
* Install Package
* Create Package Version
* Create Scratch Org
* Update Jira Issue
* Create Pull Request
* Review Pull Request
* Pull Request Exception
* Summarize Change
* List Components
* Post a Slack Message

Read below to learn about the parameters that can be customized within each Step.

## Create Change step customization

The Create Change step features three customizable parameters:

* **Name**
* **Description**
* **Source Instance (**_**required**_**)**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 5.02.01 PM.png" alt="" width="375"><figcaption></figcaption></figure>

The Source Instances that are available depend on the Salesforce environment that you are connected to.

## Create Collection step customization

The Create Change step features three customizable parameters:

* **Name**
* **Description**
* **Source Instance (**_**required**_**)**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 5.07.30 PM.png" alt="" width="375"><figcaption></figcaption></figure>

The Source Instances that are available depend on the Salesforce environment that you are connected to.

## Add Collection step customization

The Add Collection step features two customizable parameters:

* **Name**
* **Description**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 5.08.46 PM.png" alt="" width="375"><figcaption></figcaption></figure>

## Remove from Collection step customization

The Remove from Collection step features two customizable parameters:

* **Name**
* **Description**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 5.10.09 PM.png" alt="" width="375"><figcaption></figcaption></figure>

## Import Changes step customization

The Import Changes step features six customizable parameters:

* **Name**
* **Description**
* **Select Change (**_**optional**_**)**
* **Select Source Instance (**_**optional**_**)**
* **Changes filter**
* **Time range filter**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 5.12.58 PM.png" alt="" width="375"><figcaption></figcaption></figure>

The elements within the **Select Change** and **Select Source Instance** parameters are impacted by the Salesforce environment that you are connected to.

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

## Commit step customization

The Commit step features five customizable parameters:

* **Name**
* **Description**
* **Select change (**_**optional**_**)**
* **Select Source Instance (**_**optional**_**)**
* **Select Repository (**_**optional**_**)**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 5.29.06 PM.png" alt="" width="375"><figcaption></figcaption></figure>

The elements within the **Select change,** **Select Source Instance,** and **Select Repository** parameters are impacted by the Salesforce environment that you are connected to.

## Promote step customization

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

The elements within the **Select Target Instance** and **Select Change** parameters are impacted by the Salesforce environment that you are connected to.

The **Conflict resolution** parameter offers four options:

* Auto-resolve (when possible)
* Resolve manually
* Favor source branch
* Favor target branch

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

The elements within the **Select Target Instance**, **Select Collection**, and **Select Source** parameters are impacted by the Salesforce environment that you are connected to.

## Install Package step customization

The Install Package step features nine customizable parameters:

* **Name**
* **Description**
* **Select Target Instance (**_**optional**_**)**
* **Select DevHub Instance (**_**required**_**)**
* **Package Options**
* **Installation key**
* **Package access type**
* **Upgrade tupe**
* **Apex compile option**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 6.21.28 PM.png" alt="" width="375"><figcaption></figcaption></figure>

The elements within the **Select Target Instance** and **Select DevHub Instance** parameters are impacted by the Salesforce environment that you are connected to.

## Create Package Version step customization

The Create Package step features five main customizable parameters:

* **Name**
* **Description**
* **Select DevHub Instance (**_**required**_**)**
* **Source branch (**_**required**_**)**
* **Installation key**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 7.09.26 PM.png" alt="" width="375"><figcaption></figcaption></figure>

The elements within the **Select DevHub Instance** parameter are impacted by the Salesforce environment that you are connected to.

### Hidden parameters

The Create Package Version step also features ten customizable parameters that are hidden by default:

* **Definition file**
* **Tag**
* **Skip Validation** option - don't include second generation managed package (2GP) ancestors
* **Code Coverage** option - calculate and store the code coverage percentage by running the packaged Apex tests included in this package version
* **Skip Ancestor Check** option - overrides ancestry requirements, which allows you to specify a packaged ancestor that isn't the highest released package version
* **Post Install Script**
* **Uninstall Script**
* **Post Install Url**
* **Release Notes Url**
* **Language**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 7.10.20 PM.png" alt="" width="375"><figcaption></figcaption></figure>

## Create Scratch Org step customization

The Create Scratch Org step features five main customizable parameters:

* **Name**
* **Description**
* **Select DevHub Instance (**_**required**_**)**
* **Duration days**
* **Edition**
* **Options**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 7.22.31 PM.png" alt="" width="375"><figcaption></figcaption></figure>

The elements within the **Select DevHub Instance** parameter are impacted by the Salesforce environment that you are connected to.

### Edition parameter options

The **Edition** parameter offers eight options:

* Developer
* Enterprise
* Group
* Professional
* Partner Developer
* Partner Enterprise
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


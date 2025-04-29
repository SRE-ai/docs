---
description: Learn about the customizable parameters in each Trigger
---

# Triggers customization

## Overview

SRE.ai offers six different Triggers:

* [Manual](triggers-customization.md#manual-trigger-customization)&#x20;
* [Schedule](triggers-customization.md#schedule-trigger-customization)
* [Webhook](triggers-customization.md#webhook-trigger-customization)
* [Commit](triggers-customization.md#commit-trigger-customization)
* [Promote](triggers-customization.md#promote-trigger-customization)
* [Deployment](triggers-customization.md#deployment-trigger-customization)

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 1.43.59 PM.png" alt="" width="375"><figcaption></figcaption></figure>

Read below to learn about the parameters that can be customized within each Trigger

***

## Manual trigger customization

A click activates a manual trigger.

The manual trigger features one customizable parameter, a **Description.**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 2.38.30 PM.png" alt="" width="375"><figcaption></figcaption></figure>

***

## Schedule trigger customization

The Schedule trigger is scheduled with cron syntax

The Schedule trigger features three customizable parameters:

* **Description**
* **Cron expression**
* **Local running toggle**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 2.42.03 PM.png" alt="" width="375"><figcaption></figcaption></figure>

Learn more about cron syntax in [SRE.ai's cron syntax documentation](../../images-and-media/cron-syntax.md).

***

## Webhook trigger customization

<details>

<summary><mark style="background-color:yellow;"><strong>Click to learn more about the Webhook trigger</strong></mark></summary>

The Webhook trigger features two customizable parameters:

* **Description**
* **Connected application**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 2.47.17 PM.png" alt="" width="375"><figcaption></figcaption></figure>

### Webhook trigger supported applications

The Webhooks trigger can connect with three apps:

* Jira
* Github
* Bitbucket

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 2.49.46 PM.png" alt="" width="235"><figcaption></figcaption></figure>

</details>

***

## Commit trigger customization

<details>

<summary><mark style="background-color:yellow;"><strong>Click to learn more about the Commit trigger</strong></mark></summary>

The Commit trigger features three customizable parameters:

* **Description**
* **Conditions**
* **Local running toggle**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 4.29.26 PM.png" alt="" width="375"><figcaption></figcaption></figure>

By default, Commit Triggers are activated by the stated commit

### Conditions customization

Use the Conditions parameter to arrange conditions for the commit.&#x20;

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 4.31.09 PM.png" alt=""><figcaption></figcaption></figure>

A condition can be defined as being a value from one of six fields:

* Branch
* Name&#x20;
* User&#x20;
* Instance
* Package directory
* Repository

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 4.37.07 PM.png" alt=""><figcaption></figcaption></figure>

Multiple conditions can be paired with one another

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 4.39.00 PM.png" alt=""><figcaption></figcaption></figure>

Nodes are field values listed within other field values

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 4.40.29 PM.png" alt=""><figcaption></figcaption></figure>

</details>

***

## Promote trigger customization

Promote triggers feature three customizable parameters:

* **Description**
* **Conditions**
* **Local running toggle**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 4.42.05 PM.png" alt="" width="375"><figcaption></figcaption></figure>

Conditions for Promote triggers are customized like [conditions for Commit triggers.](triggers-customization.md#conditions)

***

## Deployment trigger customization

The deployment trigger features one customizable parameter, a **Description.**

<figure><img src="../../.gitbook/assets/Screenshot 2025-04-24 at 4.41.40 PM.png" alt="" width="375"><figcaption></figcaption></figure>

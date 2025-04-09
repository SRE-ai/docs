---
description: Learn how to track and manage changes in SRE.ai.
---

# Changes

## Summary

Usually, developing a new feature in Salesforce involves updating a range of metadata types and data. Moreover, there can be tasks and scripts involved. Using **Changes**, you can track the changes and instructions corresponding to every feature, big or small.

## General

You can easily select the metadata types you want to include.

Changes supports every metadata type that [Metadata API ](https://developer.salesforce.com/docs/atlas.en-us.api_meta.meta/api_meta/meta_intro.htm)supports.

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

You can import changes directly if your source environment enabled [Source Tracking](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_setup_enable_source_tracking_sandboxes.htm).

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

## Permissions

Specify and migrate access settings for Profiles and Permission Sets, including:

* Object-level permissions
* Field-level permissions
* Tab settings
* Visualforce pages
* Apex classes

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

## Data

Create a visual representation of your query by selecting specific objects and fields, navigating through parent-child relationships, and retrieving records from multiple objects in a single operation. You can configure to run either before or after metadata deployment.

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

## Apex scripts

Automate the execution of anonymous code as part of your deployment process and specify whether it should run before or after metadata deployment.

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

## Destructive changes

Track and manage destructive changes you want to make to your environment and specify whether they should be executed pre or post-deployment.

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

## Tasks

Track and manage any manual steps in your deployment process, and specify whether they should be executed before or after metadata deployment.

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>


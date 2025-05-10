# Flows cookbook

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcRWaceZaZDTb6oKsMTZ5oW8b-07Ybk7BbiKhgH2E6fD3sIZ7PO4pvsPAWkzFIxfT1nw0jL0IvuaoW3yaOxIqEskSKiNW-w_2b_r5Dn9H78tv7kozAJu5kxCGGnqR5VnS0mpsX6xg?key=KGRvWmZl-fuCdLy1wb0cBoXd)

## Overview

The SRE.ai Flows Cookbook is your launchpad for building automations.

Think of it as a collection of real-world recipes, showcasing how you can combine Triggers and Steps to streamline your DevOps workflows.

Unlike traditional cookbooks packed with code and tests, the Flows Cookbook highlights the intuitive nature of automation.

Each recipe gives you a simple blueprint of what happens, when it happens, and how it moves work forward.&#x20;

No scripting is required.

Whether you're looking to auto-promote changes after approval, sync updates to Jira, or notify your team in Slack, the Flows Cookbook outlines what's possible and sparks ideas for your own custom Flows.

Use these examples as starting points.

Tweak them. Remix them. Make them yours.

### What you’ll find

* **Pre-built Flow templates**:
  * Ready-to-deploy Flows that bundle common sequences of triggers and steps for Salesforce DevOps tasks (like promoting changes after a Pull Request is approved).
* **Trigger and Step combination outlines**:
  * Each recipe details how to set up the given Flow's Triggers and Steps
* **Customization guidance**:
  * Each recipe serves as a starting point.&#x20;
  * You can adapt and extend them by adding conditions, steps, or human-in-the-loop checkpoints to fit your specific DevOps needs.

## Example Cookbook Recipes

### Commit latest pull request

<figure><img src="../.gitbook/assets/commit-latest.png" alt="" width="375"><figcaption></figcaption></figure>

#### **Goal:**

Quickly package and commit the latest changes from your Salesforce environment, creating a pull request for review.

#### **Best for:**

Teams that want to simply the commit process, maintain clean version control, and accelerate deployment pipelines by bundling:

* Change tracking
* Imports
* Commits
* PR creation

#### **Trigger setup:**

Set up a Manual Trigger

<figure><img src="../.gitbook/assets/Screenshot 2025-04-28 at 4.13.47 PM.png" alt="" width="563"><figcaption></figcaption></figure>

#### **Steps setup:**

1. Select a Source Instance for the [Create Change Step](steps/steps-customization.md#create-change-step-customization)

<figure><img src="../.gitbook/assets/create-change-step.png" alt="" width="563"><figcaption></figcaption></figure>

2. Set the Scope and Time Range for the [Import Changes Step](steps/steps-customization.md#import-changes-step-customization)

<figure><img src="../.gitbook/assets/import-changes-step.png" alt="" width="563"><figcaption></figcaption></figure>

3. Select a Repository and Commit type for the [Commit Step](steps/steps-customization.md#commit-step-customization)

<figure><img src="../.gitbook/assets/commit-step (1).png" alt="" width="563"><figcaption></figcaption></figure>

4. Select a Connection and Destination branch for the [Create Pull Request Step](steps/steps-customization.md#create-pull-request-step-customization)

<figure><img src="../.gitbook/assets/create-pull-request-step.png" alt="" width="563"><figcaption></figcaption></figure>

### Review pull request

<figure><img src="../.gitbook/assets/review-pull-request-flow.png" alt=""><figcaption></figcaption></figure>

#### **Goal:**

Automatically review incoming pull requests to enforce best practices, streamline approvals, and generate AI-powered summaries of changes.

#### **Best for:**

Teams looking to accelerate their pull request review process while maintaining quality, consistency, and visibility into key changes.

#### **Trigger setup:**

Edit the Webhook Trigger to activate with GitHub

<figure><img src="../.gitbook/assets/Screenshot 2025-04-28 at 5.26.23 PM.png" alt=""><figcaption></figcaption></figure>

#### **Steps setup:**&#x20;

1. Edit the [Pull Request Exception Step](steps/steps-customization.md#pull-request-exception-step-customization) to Check for Skip Test by:
   1. Selecting a Connection
   2. Labelling the Pull Request Action as "Skip Test"
   3. Setting the Criteria to Exclude your selected Types

<figure><img src="../.gitbook/assets/check-for-skip-test-step.png" alt=""><figcaption></figcaption></figure>

2. Edit the Pull Request Exception Step to Check for Skip Reviews by:
   1. Selecting a Connection
   2. Labelling the Pull Request Action as "Skip Reviews"
   3. Turning the Auto Approve toggle on
   4. Setting the Criteria to Exclude your selected Types

<figure><img src="../.gitbook/assets/check-for-skip-reviews-step.png" alt="" width="563"><figcaption></figcaption></figure>

3. Edit the [Summarize Change Step](steps/steps-customization.md#summarize-change-step-customization) by:
   1. Selecting a Connection
   2. Selecting Key Changes and Implementation Details as Summary topics
   3. Selecting SRE.ai Salesforce 1.0 as an AI model

<figure><img src="../.gitbook/assets/summarize-change-step.png" alt="" width="563"><figcaption></figcaption></figure>

### Update Jira issue after deployment

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcpWdjMREovieRd2MiMuc8iluIBHUgQlpPJzDDOm529K7KlVEn0H2rJfyJiZCNhxFXUe-Z4e6gTf13lJCUti_XOY-dLv9vdjJaBeuYnmaLS90Xyzrjktms18f9HJcsZ1o1-pEKk6A?key=KGRvWmZl-fuCdLy1wb0cBoXd" alt="" width="375"><figcaption></figcaption></figure>

#### **Goal:**

After successfully deploying a Collection, automatically update the corresponding Jira ticket to reflect the deployment status.

#### **Best for:**

Teams using Jira to track release readiness and QA coordination.

#### **Trigger:**

Edit the Promote Trigger to activate when a collection is deployed

<figure><img src="../.gitbook/assets/Screenshot 2025-04-28 at 11.47.12 AM.png" alt="" width="375"><figcaption></figcaption></figure>

**Steps:**

1. Edit the [Update Jira Issue Step's](steps/steps-customization.md#update-jira-issue-step-customization) mapping to update the relevant issue's status as QA

<figure><img src="../.gitbook/assets/Screenshot 2025-04-28 at 11.46.50 AM.png" alt="" width="375"><figcaption></figcaption></figure>

***

### Update collection

<figure><img src="../.gitbook/assets/update-collection-flow.png" alt=""><figcaption></figcaption></figure>

**Goal:**\
Automatically keep Collections in sync with active Jira issues by adding relevant issues when created or updated, and promptly removing them when conditions change. Ensure Collections reflect only current, actionable work.

**Best for:**\
Teams managing dynamic workspaces who want to automate the tracking of Sprint-related Jira issues without manually maintaining Collections.

**Trigger:**

Edit the Webhook Trigger to activate when a Jira issue that starts with "CRM" is assigned to a sprint and is newly created or updated

<figure><img src="../.gitbook/assets/Screenshot 2025-04-28 at 7.14.32 PM.png" alt="" width="353"><figcaption></figcaption></figure>

**Steps:**

1. Set up an [Add to Collection Step](steps/steps-customization.md#add-to-collection-step-customization)**.** The Add to Collection Step adds the relevant Jira issue to a relevant Collection

<figure><img src="../.gitbook/assets/Screenshot 2025-04-28 at 7.39.59 PM.png" alt=""><figcaption></figcaption></figure>

2. Set up a [Remove from Collection Step](steps/steps-customization.md#remove-from-collection-step-customization). The Remove from Collection Step removes the relevant Jira issue to clean up the Collection once the condition changes or is no longer relevant

<figure><img src="../.gitbook/assets/Screenshot 2025-04-28 at 7.40.04 PM.png" alt=""><figcaption></figcaption></figure>


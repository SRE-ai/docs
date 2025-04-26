# Flows cookbook

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcRWaceZaZDTb6oKsMTZ5oW8b-07Ybk7BbiKhgH2E6fD3sIZ7PO4pvsPAWkzFIxfT1nw0jL0IvuaoW3yaOxIqEskSKiNW-w_2b_r5Dn9H78tv7kozAJu5kxCGGnqR5VnS0mpsX6xg?key=KGRvWmZl-fuCdLy1wb0cBoXd)

## What is the Flows Cookbook?

The Flows Cookbook offers curated, ready-to-use templates for building Flows faster and more reliably.&#x20;

Instead of designing every automation from scratch, users can start with a preconfigured combination of triggers and steps that solve common DevOps scenarios.

Think of the Cookbook as your collection of recipes, examples of best practices you can apply, modify, and scale as your workflows grow more complex.

***

## What You’ll Find in the Cookbook

* **Pre-built Flow templates**:
  * Ready-to-deploy Flows that bundle common sequences of triggers and steps for Salesforce DevOps tasks (like promoting changes after a Pull Request is approved).
* **Trigger and step combinations**:
  * Each recipe outlines a logical chain of automation: when a specific trigger occurs (e.g., a commit to a branch), a sequence of steps (e.g., create a pull request, promote changes, update a Jira issue) automatically follows.
* **Customization guidance**:
  * Each recipe serves as a starting point. You can adapt and extend them by adding conditions, steps, or human-in-the-loop checkpoints to fit your specific DevOps needs.
* **Best practice notes**:
  * Learn how experienced teams structure automations to maximize efficiency, reliability, and auditability, especially in high-change environments like Salesforce.

***

## Why Use the Cookbook?

* **Faster Setup**: Quickly launch common workflows without reinventing the wheel.
* **Consistency**: Standardize how Flows are built across your team.
* **Scalability**: Grow your automations easily by building off trusted templates.
* **Reduced Error Risk**: Follow proven patterns that minimize mistakes in complex deployments.

***

## Example Cookbook Recipes

### Update Jira Issue After Deployment

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcpWdjMREovieRd2MiMuc8iluIBHUgQlpPJzDDOm529K7KlVEn0H2rJfyJiZCNhxFXUe-Z4e6gTf13lJCUti_XOY-dLv9vdjJaBeuYnmaLS90Xyzrjktms18f9HJcsZ1o1-pEKk6A?key=KGRvWmZl-fuCdLy1wb0cBoXd" alt="" width="375"><figcaption></figcaption></figure>

**Goal:**\
After successfully deploying a Collection, automatically update the corresponding Jira ticket to reflect the deployment status.

**Trigger:**

* A Collection deploys

**Steps:**

1. Update the related Jira Issue (e.g., transition status to "Deployed to QA" or "Ready for Testing").
2. Add a comment linking the deployment record or Collection ID.

**Best for:**\
Teams using Jira to track release readiness and QA coordination.

***

\



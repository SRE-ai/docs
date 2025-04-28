# Flows cookbook

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcRWaceZaZDTb6oKsMTZ5oW8b-07Ybk7BbiKhgH2E6fD3sIZ7PO4pvsPAWkzFIxfT1nw0jL0IvuaoW3yaOxIqEskSKiNW-w_2b_r5Dn9H78tv7kozAJu5kxCGGnqR5VnS0mpsX6xg?key=KGRvWmZl-fuCdLy1wb0cBoXd)

## Overview

The SRE.ai Cookbook is your launchpad for building smarter, faster automations.

Think of it as a collection of real-world recipes, showcasing how you can combine **Triggers** (the events that kick things off) and **Steps** (the actions that follow) to streamline your DevOps workflows.

Unlike traditional "cookbooks" packed with code and tests, SRE.ai makes automation **intuitive**.&#x20;

Each recipe gives you a simple blueprint: what happens, when it happens, and how it moves work forward.&#x20;

No scripting required.

Whether you're looking to **auto-promote changes after approval**, **sync updates to Jira**, or **notify your team in Slack**, our Cookbook helps you see what's possible and sparks ideas for your own custom Flows.

Use these examples as starting points.

Tweak them. Remix them. Make them yours.

### What you’ll find

* **Pre-built Flow templates**:
  * Ready-to-deploy Flows that bundle common sequences of triggers and steps for Salesforce DevOps tasks (like promoting changes after a Pull Request is approved).
* **Trigger and step combination outlines**:
  * Each recipe outlines a logical chain of automation: when a specific trigger occurs (e.g., a commit to a branch), a sequence of steps (e.g., create a pull request, promote changes, update a Jira issue) automatically follows.
* **Customization guidance**:
  * Each recipe serves as a starting point. You can adapt and extend them by adding conditions, steps, or human-in-the-loop checkpoints to fit your specific DevOps needs.

***

## Example Cookbook Recipes

### Update Jira Issue After Deployment

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcpWdjMREovieRd2MiMuc8iluIBHUgQlpPJzDDOm529K7KlVEn0H2rJfyJiZCNhxFXUe-Z4e6gTf13lJCUti_XOY-dLv9vdjJaBeuYnmaLS90Xyzrjktms18f9HJcsZ1o1-pEKk6A?key=KGRvWmZl-fuCdLy1wb0cBoXd" alt="" width="375"><figcaption></figcaption></figure>

**Goal:**\
After successfully deploying a Collection, automatically update the corresponding Jira ticket to reflect the deployment status.

**Best for:**\
Teams using Jira to track release readiness and QA coordination.

**Trigger:**

* A Collection deploys

<figure><img src="../.gitbook/assets/Screenshot 2025-04-28 at 11.47.12 AM.png" alt="" width="375"><figcaption></figcaption></figure>

**Steps:**

1. Update the related Jira Issue (e.g., transition status to "Deployed to QA" or "Ready for Testing").
2. Add a comment linking the deployment record or Collection ID.

<figure><img src="../.gitbook/assets/Screenshot 2025-04-28 at 11.46.50 AM.png" alt="" width="375"><figcaption></figcaption></figure>

***

\



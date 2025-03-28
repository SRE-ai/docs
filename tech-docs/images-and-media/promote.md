---
description: >-
  Learn how to merge branches, resolve conflicts, and promote changes through
  the environment chain in SRE.ai.
---

# Promote

Promote lets you move changes forward or backward in the environment chain while managing Git workflows in the background.

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

SRE.ai makes promoting a Change, Collection, or Branch easy and handles the complex tasks behind the scenes. Complex tasks may include:

* Merging the feature branch
* Resolving merge conflicts with patches (when available)
* Creating deployment artifacts
* Deploying to the target environment
* Cleaning up branches

The entire process is streamlined, with steps executing one after the other.

Promoting a Change, Collection, or Branch merges its associated feature branch(es) into the target branch.

To ensure a successful deployment, SRE.ai:

1. Creates a temporary branch from the target branch
2. Merges the feature branch(es) into the temporary branch
3. Deploys the resulting package artifact(s) to the target branch

If the deployment succeeds, the temporary branch is merged into the target branch.

You can view the progress at each step in the execution log, which includes information about:

* Git commands
* Metadata deployment
* Data updates
* Task or script execution

The deployment log is also available for reference under the deployment record created for each promotion.

SRE.ai maintains a record of the deployment log and build artifacts for every deployment or validation.

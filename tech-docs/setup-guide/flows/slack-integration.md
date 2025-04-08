# Slack integration

## Overview

Learn how to set up SRE.ai in Slack.

## **Salesforce Setup**

1. Add a [Remote Site Setting](https://help.salesforce.com/s/articleView?id=xcloud.configuring_remoteproxy.htm\&type=5) in Salesforce:
   * Remote Site Name: Slack
   * Remote Site URL:[ https://slack.com](https://slack.com)

## **Slack App Configuration**

### Create a new Slack app

1. Click the workspace dropdown
2. Click **Tools & Settings**
3. Click **Manage Apps**
4. Click the **Build** link
5. Click **Create New App**
6. Click the **From Scratch** option
7. Name your app "SRE"
8. Select your workspace
9. Click **Create App**
10. Add the shared image in the Display Information Section

### Configure app permissions:

1. Enter the **App Details** screen
2. Select **OAuth & Permissions**

* Scroll to the "Scopes" section
* Add the OAuth Scope: "chat:write"
* Return to the top of the "OAuth Token" section
* Click "Install to \[your workspace name]."
* Confirm by clicking "Allow"
* Now copy the Bot User OAuth Token for later use

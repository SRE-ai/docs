---
description: Learn how to set up SRE.ai in Slack.
---

# Slack flow

## **Salesforce Setup**

1. Add a [Remote Site Setting](https://help.salesforce.com/s/articleView?id=xcloud.configuring_remoteproxy.htm\&type=5) in Salesforce:
   * Remote Site Name: Slack
   * Remote Site URL:[ https://slack.com](https://slack.com)

***

## **Slack App Configuration**

### Create a new Slack app

1. Click the **Workspace dropdown**
2. Click **Tools & Settings**
3. Click **Manage Apps**
4. Click the **Build** link
5. Click **Create New App**
6. Select the **From Scratch** option
7. Name your app **"SRE"**
8. Select your workspace
9. Click **Create App**
10. Add the shared image in the **Display Information Section**

### Configure app permissions:

1. Enter the **App Details** screen
2. Select **OAuth & Permissions**
3. Scroll to the **Scopes** section
4. Add the following **OAuth Scope:** "chat:write"
5. Scroll to the top of the **OAuth Token** section
6. Click **Install to \[your workspace name].**
7. Click **Allow**
8. Take note of the **Bot User OAuth Token** for later use

***

## Slack channel setup

1. Create a private Slack channel

{% hint style="info" %}
**IMPORTANT:** Take note of the Slack channel's name
{% endhint %}

2. Invite the SRE bot to your channel
   1. Type "@SRE" in the chat
   2. Accept Slack's prompt to invite the bot

***

## SRE.ai web app configuration

1. Click **Manage \[your workspace]** in the SRE web application
2. Select **Connections**
3. Click **Add Connection**
4. Select **Slack** as the **connection type**
5. Name the connection **"Slack"**
6. Paste the [OAuth token you noted earlier](slack-flow.md#configure-app-permissions)
7. Click **Save**

***

## SRE.ai web app Flow configuration

### Create a Flow

1. Create a new Flow named **"slack-deployment-notification"**
2. Click **Continue**

### Configure the Flow

1. Set the Trigger as a [**Promote Trigger**](triggers/triggers-customization.md#promote-trigger-customization)
2. Add the [**Post a Slack Message Step**](steps/steps-customization.md#post-slack-message-step-customization)
   1. Select **Slack** as the **Connection**
   2. Set the channel as [the private channel you previously named](slack-flow.md#slack-channel-setup)
3. Click **Save**
4. Click [**Activate flow**](./#create-new-flow)

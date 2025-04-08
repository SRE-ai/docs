# Slack integration

## Overview

Learn how to set up SRE.ai in Slack.

## **Salesforce Setup**

1. Add a [Remote Site Setting](https://help.salesforce.com/s/articleView?id=xcloud.configuring_remoteproxy.htm\&type=5) in Salesforce:
   * Remote Site Name: Slack
   * Remote Site URL:[ https://slack.com](https://slack.com)

## **Slack App Configuration**

### Create a new Slack app

1. Click the **Workspace dropdown**
2. Click **Tools & Settings**
3. Click **Manage Apps**
4. Click the **Build** link
5. Click **Create New App**
6. Select the **From Scratch** option
7. Name your app "SRE"
8. Select your workspace
9. Click **Create App**
10. Add the shared image in the **Display Information Section**

### Configure app permissions:

1. Enter the **App Details** screen
2. Select **OAuth & Permissions**
3. Scroll to the **Scopes** section
4. Add the **OAuth Scope:** "chat:write"
5. Scroll to the top of the **OAuth Token** section
6. Click **Install to \[your workspace name].**
7. Click **Allow**
8. Take note of the **Bot User OAuth Token** for later use

## Slack channel setup

1. Create a private Slack channel, keep the name handy for later steps
2. Invite the bot to your channel:

* Type "@SRE" in the chat
* Accept Slack's prompt to invite the bot

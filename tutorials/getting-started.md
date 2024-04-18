---
title: 🛠 Getting Started
published: true
date: 2024-02-15T21:13:42.617Z
tags: null
editor: markdown
dateCreated: 2023-08-19T00:07:55.122Z
description: >-
  Start using Sonoran Bot to link Sonoran products to your discord and perform
  common moderation actions.
---

# Getting Started

Sonoran Bot supports either CAD or CMS syncing. The below tutorial applies to both syncing methods; afterwards, follow the appropriate link to set up the syncing you wish to use.

{% hint style="warning" %}
All commands require at least the `Manage Server` permission on the Discord server you are running the commands in. You will also need a number of other permissions upon inviting the bot.
{% endhint %}

### 1. Invite the Bot to Your Server

[Invite the bot to your Discord server](https://sonoranbot.com/invite). You must have the "Manage Server" permission to add bots; plus any permissions the bot requires to function. You will also be joined to our support server (Sonoran Software Systems) automatically.

### 2. Run the Settings Command

1. After inviting the bot, run the `/settings` command. You will then be prompted to select a logging channel for Sonoran Bot to use.

![bot\_setloggingchannel.png](getting-started/bot\_setloggingchannel.png)

2. Determine which syncing method you wish to use; you may set up both community types.
   1. Enter your [Sonoran CAD ID and API key](https://info.sonorancad.com/sonoran-cad/api-integration/getting-started/retrieving-your-credentials).
   2. AND/OR Enter your [Sonoran CMS ID and API key](https://info.sonorancms.com/developer-api-documentation/api-integration/getting-started#gather-your-credentials).

![screenshot\_11.png](getting-started/bot\_setuppage.png)

Click `Submit` and the setup is now complete.

{% hint style="info" %}
If you set up both CMS and CAD, the Discord bot will automatically use CMS mode. Otherwise, it will use the successfully set up mode.
{% endhint %}

### 3. Invite to Additional Servers

If your community uses multiple discord servers, you can link them all to the same community to utilize the permissions sync easily. Simply set them up normally as you just did, and they will automatically be synced! You will be able to use the bot's commands just like on the primary server.

### 4. Set up Integrations

At this point, you will need to select either CAD or CMS integration. We highly encourage users to make use of the CMS integration as the CMS can integrate with the CAD on its own!

* [CMS Integration](sonoran-cms-integration.md)&#x20;
* [CAD Integration](sonoran-cad-integration.md)&#x20;
* [Settings](usage/settings.md)&#x20;
* [Commands](usage/commands.md)

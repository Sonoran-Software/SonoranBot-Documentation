---
title: getting-started
description: 
published: true
date: 2023-09-05T18:32:50.088Z
tags: 
editor: markdown
dateCreated: 2023-08-19T00:07:55.122Z
---

# 🛠 Getting Started

Sonoran Bot supports either CAD or CMS syncing. The below tutorial applies to both syncing methods; afterwards, follow the appropriate link to set up the syncing you wish to use.

> All commands require at least the Manage Server permission on the Discord server you are running the commands in. You will also need a number of other permissions upon inviting the bot.
{.is-warning}
### 1. Invite the Bot to Your Server

[Invite the bot to your Discord server](https://discord.com/api/oauth2/authorize?client\_id=1060274480930361424\&permissions=9395244032\&scope=bot%20applications.commands). You must have the "Manage Server" permission to add bots; plus any permissions the bot requires to function.

### 2. Run the Setup Command

1. After inviting the bot, run the `/setup` command.
2.  Determine which syncing method you wish to use; you may set up both community types.

    1. Enter your [Sonoran CAD ID and API key](https://info.sonorancad.com/sonoran-cad/api-integration/getting-started/retrieving-your-credentials).
    2. AND/OR Enter your [Sonoran CMS ID and API key](https://info.sonorancms.com/developer-api-documentation/api-integration/getting-started#gather-your-credentials).

![screenshot_11.png](/screenshot_11.png)

You will then be presented with the results of the setup.

![image.png](/image.png)

> If you set up both CMS and CAD, the Discord bot will automatically use CMS mode. Otherwise, it will use the successfully set up mode.
{.is-info}

### 3. Invite to Additional Servers

If your community uses multiple discord servers, you can link them all to the same community to utilize the permissions sync easily using the `/guildlink` command, as shown below.

![guildlink.png](/guildlink.png)

Fill out the information (using either your CAD or CMS information), and you will receive a confirmation. At this point, you can use the other commands just like on the primary server.

### 4. Set up Integrations

At this point, you will need to select either CAD or CMS integration. We highly encourage users to make use of the CMS integration as the CMS can integrate with the CAD on its own!

[CMS Integration](/tutorials/getting-started/sonoran-cms-integration)
[CAD Integration](/tutorials/getting-started/sonoran-cad-integration)
[Community Management](/tutorials/getting-started/community-management/getting-started)

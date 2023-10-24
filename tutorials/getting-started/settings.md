---
title: Settings
description: 
published: true
date: 2023-10-24T19:40:34.121Z
tags: 
editor: markdown
dateCreated: 2023-08-19T00:08:01.094Z
---

# Sonoran Bot Settings

Running the command `/settings` allows you to manage many different aspects of how Sonoran Bot interacts with your Discord and CMS.

![bot_settings.png](/tutorials/getting-started/settings/bot_settings.png)

## API Settings

Within the `/settings` menu, you can select API Settings, which will give you the options to change or delete the settings for your linked CAD and CMS communities.

![bot_apisettings.png](/tutorials/getting-started/settings/bot_apisettings.png)

## CMS Settings

Within the `/settings` menu, you can select CMS Settings to change different settings related to how Sonoran Bot syncs with your CMS community. Within this menu, you can customize settings in the following categories:

### Calendar Events

Allows you to toggle sync between CMS calendar events and your Discord. Enabling this will create a Discord event for any calendar events created in CMS.

### Name Sync

Allows you to toggle Name Sync. Enabling this will automatically change the nicknames of all users in the server to their corresponding CMS account names.

### SonoranCMS Forms -> Discord

![bot_cmsformsdiscord.png](/tutorials/getting-started/settings/bot_cmsformsdiscord.png)

#### Form Response Mode

Allows you to choose how webhook for form reponses are delivered. The options are as follows:
- Discord Direct Message
- Discord Channel
- Both

#### Form Response Channel

If you've selected `Discord Channel` or `Both` in Form Repsonse Mode, this is where you select the channel that the webhooks send to.

![bot_formresponsemsg.png](/tutorials/getting-started/settings/bot_formresponsemsg.png)

#### Form Response Fallback Channel

### Clock In/Out

Toggles the ability to clock in and out in CMS from Discord. If enabled, users can do `/clockincms` to clock in or `/clockoutcms` to clock out. This will automatically send clock information to CMS.

## Role Sync Settings

### Toggle Strip Unmapped
If enabled will automatically remove permissions from users who do not have a matching secret key to their Discord ID. This is only relevant if using CAD sync.
### Toggle Kick On Leave 
If enabled will automatically remove a user from CMS if they leave or are banned from the Discord.

## Logging Settings

Allows you to set or change the General logging channel and the Moderation logging channel.

![bot_setloggingchannel.png](/tutorials/getting-started/settings/moderation/bot_setloggingchannel.png)
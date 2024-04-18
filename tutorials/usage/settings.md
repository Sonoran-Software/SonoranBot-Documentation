---
title: Settings
published: true
date: 2023-10-26T19:11:28.315Z
tags: null
editor: markdown
dateCreated: 2023-08-19T00:08:01.094Z
description: Learn more about SonoranBot's different settings.
---

# Settings

Running the command `/settings` allows you to manage many different aspects of how Sonoran Bot interacts with your Discord and CMS.

![SonoranBot - /settings command](../getting-started/settings/bot\_settings.png)

## API Settings <a href="#api-settings" id="api-settings"></a>

Within the `/settings` menu, you can select API Settings, which will give you the options to change or delete the settings for your linked CAD and CMS communities.

![SonoranBot - API Settings](../getting-started/settings/bot\_apisettings.png)

## CMS Settings <a href="#cms-settings" id="cms-settings"></a>

Within the `/settings` menu, you can select CMS Settings to change different settings related to how Sonoran Bot syncs with your CMS community. Within this menu, you can customize settings in the following categories:

### Calendar Events <a href="#calendarevents-settings" id="calendarevents-settings"></a>

Allows you to toggle sync between CMS calendar events and your Discord. Enabling this will create a Discord event for any calendar events created in CMS.

### Name Sync <a href="#namesync-settings" id="namesync-settings"></a>

Allows you to toggle Name Sync. Enabling this will automatically change the nicknames of all users in the server to their corresponding CMS account names.

### SonoranCMS Forms -> Discord <a href="#cmsforms-settings" id="cmsforms-settings"></a>

Sonoran Bot can now ping users on Discord when their form or application statuses are updated in CMS. This menu allows you to set the form response mode, channel and fallback channel.

![SonoranBot - CMS Forms -> Discord Settings](../../.gitbook/assets/Bot\_CMSFormsDiscord.png)

#### Form Response Mode

Allows you to choose how webhook for form responses are delivered. The options are as follows:

* Discord Direct Message
* Discord Channel
* Both

#### Form Response Channel

If you've selected `Discord Channel` or `Both` in Form Respsonse Mode, this is where you select the channel that the webhooks send to.

![SonoranBot - Form Response Message](../getting-started/settings/bot\_formresponsemsg.png)

#### Form Response Fallback Channel

### Clock In/Out <a href="#cmsclock-settings" id="cmsclock-settings"></a>

Toggles the ability to clock in and out in CMS from Discord. If enabled, users can do `/clockincms` to clock in or `/clockoutcms` to clock out. This will automatically send clock information to CMS.

## Role Sync Settings <a href="#role-sync-settings" id="role-sync-settings"></a>

### Toggle Strip Unmapped

If enabled will automatically remove permissions from users who do not have a matching secret key to their Discord ID. This is only relevant if using CAD sync.

### Toggle Kick On Leave

If enabled will automatically remove a user from CMS if they leave or are banned from the Discord.

## Logging Settings <a href="#logging-settings" id="logging-settings"></a>

Allows you to set or change the General logging channel and the Moderation logging channel.

![SonoranBot - Set Logging Channel](../getting-started/settings/moderation/bot\_setloggingchannel.png)

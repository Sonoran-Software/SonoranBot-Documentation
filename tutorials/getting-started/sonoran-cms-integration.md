---
title: Sonoran CMS Integration
description: Link Sonoran Bot to Sonoran CMS for role syncing and other handy features!
published: true
date: 2023-11-22T19:13:46.161Z
tags: 
editor: markdown
dateCreated: 2023-08-19T00:08:23.412Z
---

# Video Guide

Sync your Discord roles with SonoranCMS permissions!

https://www.youtube.com/watch?v=jmA6CMfuq4E

# Getting Started <a href="#getting-started" id="getting-started"></a>

By default, **only Administrators of the Discord guild can access the commands** below. These can be changed in the Settings menu of the server.

## 1. Discord SSO Linking <a href="#1.-discord-sso-linking" id="1.-discord-sso-linking"></a>

Users must link their Discord to their Sonoran account. This will also automatically add their Discord [API ID](https://info.sonorancms.com/developer-api-documentation/api-integration/getting-started/api-id-system).

**Enable Discord Sync**

* In the Administration Panel, under Advanced navigate to `Integrations` > `Discord`
* Click `Refresh Data` to sync your CMS Community with your Discord.

![cms_botrefreshdata.png](/tutorials/getting-started/sonoran-cms-integration/cms_botrefreshdata.png)

**Link your Discord Account**

Once enabled in the CMS, users who do not yet have their Discord account linked with their Sonoran account will see the following banner:

![Bot_LinkDiscordCMS.png](/tutorials/getting-started/sonoran-cms-integration/Bot_LinkDiscordCMS.png)

## 2. Role Mapping <a href="#2.-role-mapping" id="2.-role-mapping"></a>

The command `/rolemap` can now be used.

The following image is when a CMS mode is selected.

![Bot_CMSRolemap01.png](/tutorials/getting-started/sonoran-cms-integration/bot_cmsrolemap01.png)

Select a department, rank you wish to modify, and the role you wish to apply to the rank.

![Bot_CMSRolemap02.png](/tutorials/getting-started/sonoran-cms-integration/bot_cmsrolemap02.png)

The `Set Department-wide Role` button will automatically assign the role you select to the selected department (in this case, `Civilian Department`).

![Bot_CMSRolemap03.png](/tutorials/getting-started/sonoran-cms-integration/bot_cmsrolemap03.png)

There will be left and right arrows to page if you have more than 25 roles.

![Bot_CMSRolemap04.png](/tutorials/getting-started/sonoran-cms-integration/bot_cmsrolemap04.png)

![Bot_CMSRolemap05.png](/tutorials/getting-started/sonoran-cms-integration/bot_cmsrolemap05.png)

In this example, having `Staff` Role in Discord will get the rank `Civilian Director` in the CMS.

At any time, you can change the dropdowns to select another Department or Rank.

# Role Syncing <a href="#role-syncing" id="role-syncing"></a>

> Unlike the CAD sync mode, users will not use the `/linkme` command - this is handled within the Sonoran Account SSO.
{.is-info}

After setting up the above, the command `/sync` will set up everyone's permissions.

# Features <a href="#features" id="features"></a>

All the below features can be changed through the `/settings` menu described [here](/tutorials/getting-started/settings#cms-settings).

- Sonoran Bot can now ping users on Discord when their form or application statuses are updated in CMS. 
- Sonoran Bot syncs calendar events created in your CMS by automatically creating an event in your discord server.
- If enabled, Sonoran Bot syncs the names of your CMS users with their Discord account. Their Discord accounts are automatically given nicknames accordingly.
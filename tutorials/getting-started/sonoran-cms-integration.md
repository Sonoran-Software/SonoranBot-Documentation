---
title: Sonoran CMS Integration
description: Link Sonoran Bot to Sonoran CMS for role syncing and other handy features!
published: true
date: 2023-10-10T22:40:28.937Z
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

![Bot_Rolemap01.png](/tutorials/getting-started/sonoran-cms-integration/Bot_Rolemap01.png)

Select a department, rank you wish to modify, and the role you wish to apply to the rank.

![Bot_Rolemap02.png](/tutorials/getting-started/sonoran-cms-integration/Bot_Rolemap02.png)

The `Set Department-wide Role` button will automatically assign the Department (in this example, Community Leadership) to anyone with the role you select.

![Bot_Rolemap03.png](/tutorials/getting-started/sonoran-cms-integration/Bot_Rolemap03.png)

Use the left and right arrows to page if you have more than 25 roles.

![Bot_Rolemap04.png](/tutorials/getting-started/sonoran-cms-integration/Bot_Rolemap04.png)

![Bot_Rolemap05.png](/tutorials/getting-started/sonoran-cms-integration/Bot_Rolemap05.png)

In this example, having "Staff Role" in Discord will get the rank "Director" in the CMS.

At any time, you can change the dropdowns to select another Department or Rank.

# Role Syncing <a href="#role-syncing" id="role-syncing"></a>

> Unlike the CAD sync mode, users will not use the `/linkme` command - this is handled within the Sonoran Account SSO.
{.is-info}

After setting up the above, the command `/syncroles` will set up everyone's permissions.

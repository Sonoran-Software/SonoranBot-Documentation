---
title: Sonoran CMS Integration
description: Link Sonoran Bot to Sonoran CMS for role syncing and other handy features!
published: true
date: 2024-02-06T23:22:00.245Z
tags: 
editor: markdown
dateCreated: 2023-08-19T00:08:23.412Z
---

# Video Guide

Sync your Discord roles with SonoranCMS permissions!

https://www.youtube.com/watch?v=YeCYmEnA7IA

# Getting Started <a href="#getting-started" id="getting-started"></a>

By default, **only Administrators of the Discord guild can access the commands** below. These can be changed in the Settings menu of the server.

## 1. Discord SSO Linking <a href="#1.-discord-sso-linking" id="1.-discord-sso-linking"></a>

Users must link their Discord to their Sonoran account. This will also automatically add their Discord [API ID](https://info.sonorancms.com/developer-api-documentation/api-integration/getting-started/api-id-system).

**Enable Discord Sync**

* In the Administration Panel, under Advanced navigate to `Integrations` > `Discord`
* Click `Refresh Data` to sync your CMS Community with your Discord.

![cms_botrefreshdata.png](/tutorials/getting-started/sonoran-cms-integration/cms_botrefreshdata.png)

**Link your Discord Account**

Once the bot has been added and linked to CMS, any users who do not yet have their Discord account linked with their Sonoran account will see the following banner:

![Bot_LinkDiscordCMS.png](/tutorials/getting-started/sonoran-cms-integration/Bot_LinkDiscordCMS.png)

They will be required to link their discord in order for the bot's features to work on them. This banner will show until they link their Discord to their Sonoran account.

## 2. Role Mapping <a href="#2.-role-mapping" id="2.-role-mapping"></a>

The command `/rolemap` can now be used.

![Bot_CMSRolemap01.png](/tutorials/getting-started/sonoran-cms-integration/bot_cmsrolemap01.png)

Select a department, the rank you wish to modify, and the role you wish to apply to the rank.

There will be left and right arrows to page if you have more than 25 roles.

![Bot_CMSRolemap03.png](/tutorials/getting-started/sonoran-cms-integration/bot_cmsrolemap03.png)

![Bot_CMSRolemap04.png](/tutorials/getting-started/sonoran-cms-integration/bot_cmsrolemap04.png)

In this example, having `Staff` Role in Discord will get the rank `Civilian Director` in the CMS:

![Bot_CMSRolemap05.png](/tutorials/getting-started/sonoran-cms-integration/bot_cmsrolemap05.png)


At any time, you can change the dropdowns to select another Department or Rank.

There is ample room for specific customization with role mapping. You can map multiple roles to the same rank and multiple ranks to one role should you so desire. 

Keep in mind that sync is bi-directional, so if multiple ranks are mapped to one role (or vice versa) then granting a member one rank will grant them the associated role, which will subsequently grant them the other ranks mapped to the same role.

If you wish to remove a mapping, you can select the Role whose mapping you would like to remove and click the red `Clear Mapping` button.

![bot_rolemapclear.png](/tutorials/getting-started/sonoran-cms-integration/bot_rolemapclear.png)

# Role Syncing <a href="#role-syncing" id="role-syncing"></a>

> Unlike the CAD sync mode, users will not use the `/linkme` command - this is handled within the Sonoran Account SSO.
{.is-info}

After setting up the above, the command `/sync` will set up everyone's permissions.

Setting the flag `community` to `Yes` will sync your entire community including any linked guilds. Setting it to no or running `/sync` by itself will only sync the server you run it in.

After the initial sync, changes in role mappings will generally sync themselves automatically.

# Features <a href="#features" id="features"></a>

All the below features can be changed through the `/settings` menu described [here](/tutorials/getting-started/settings#cms-settings).

- Sonoran Bot can now ping users on Discord when their form or application statuses are updated in CMS. 
- Sonoran Bot syncs calendar events created in your CMS by automatically creating an event in your discord server.
- If enabled, Sonoran Bot syncs the names of your CMS users with their Discord account. Their Discord accounts are automatically given nicknames accordingly.

# Role Mapping in CMS <a href="#role-mapping-in-cms" id="role-mapping-in-cms"></a>

You can also configure rolemapping from within CMS as well. 

This window can be accessed from CMS in `Admin Panel` > `Integrations` > `Discord` > `Role Mapping`

Here you can view all mapped ranks and what Discord roles they're mapped to, as well as add or delete mappings.

![botcms_rolemap_1.png](/tutorials/getting-started/sonoran-cms-integration/botcms_rolemap_1.png)

To add a new mapping, first start by selecting a rank:

![botcms_rolemap_2.png](/tutorials/getting-started/sonoran-cms-integration/botcms_rolemap_2.png)

Next, select the Discord role(s) you wish to map this rank to:

![botcms_rolemap_3-1.png](/tutorials/getting-started/sonoran-cms-integration/botcms_rolemap_3-1.png)
> **Hint:** You can select multiple roles to map to one rank. However, you can't select multiple ranks at once.
>Thus, if you want to map multiple ranks to one role, you will have to create a separate entry for every rank you wish to map. {.is-info}

When you're ready to create the mapping, click the `Add` button on the right-hand side.

![botcms_rolemap_4.png](/tutorials/getting-started/sonoran-cms-integration/botcms_rolemap_4.png)

When you've clicked `Add`, it will show in the list alongside all previously existing mappings.

![botcms_rolemap_5-1-1.png](/tutorials/getting-started/sonoran-cms-integration/botcms_rolemap_5-1-1.png)

At any time, you can add additional Discord roles to an existing Rank mapping by clicking the plus button.

![botcms_rolemap_6.png](/tutorials/getting-started/sonoran-cms-integration/botcms_rolemap_6.png)

This will open up a dropdown where you can select additional Discord roles to map.

![botcms_rolemap_7-2.png](/tutorials/getting-started/sonoran-cms-integration/botcms_rolemap_7-2.png)

When you've selected all desired roles, click outside and it will automatically save your new mapping.

![botcms_rolemap_8-1.png](/tutorials/getting-started/sonoran-cms-integration/botcms_rolemap_8-1.png)
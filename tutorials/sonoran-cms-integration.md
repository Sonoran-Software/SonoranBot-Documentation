---
title: Sonoran CMS Integration
published: true
date: 2024-03-19T18:12:07.885Z
tags: null
editor: markdown
dateCreated: 2023-08-19T00:08:23.412Z
description: Link Sonoran Bot to Sonoran CMS for role syncing and other handy features!
---

# Sonoran CMS Integration

## Video Guide

Sync your Discord roles with SonoranCMS permissions!

{% embed url="https://youtu.be/JbBuSGiyWvc" %}

## Getting Started <a href="#getting-started" id="getting-started"></a>

By default, **only Administrators of the Discord guild can access the commands** below. These can be changed in the Settings menu of the server.

### Discord SSO Linking <a href="#id-1.-discord-sso-linking" id="id-1.-discord-sso-linking"></a>

Users must link their Discord to their Sonoran account. This will also automatically add their Discord [API ID](https://info.sonorancms.com/developer-api-documentation/api-integration/getting-started/api-id-system).

**Enable Discord Sync**

* In the Administration Panel, under Advanced navigate to `Integrations` > `Discord`
* Click `Refresh Data` to sync your CMS Community with your Discord.

![Sonoran CMS - Refresh Discord Data](getting-started/sonoran-cms-integration/cms\_botrefreshdata.png)

**Link your Discord Account**

Once the bot has been added and linked to CMS, any users who do not yet have their Discord account linked with their Sonoran account will see the following banner:

![Sonoran CMS - Link Discord Prompt](getting-started/sonoran-cms-integration/Bot\_LinkDiscordCMS.png)

They will be required to link their discord in order for the bot's features to work on them. This banner will show until they link their Discord to their Sonoran account.

### Role Mapping in CMS <a href="#role-mapping-in-cms" id="role-mapping-in-cms"></a>

You can also configure rolemapping from within CMS as well.

This window can be accessed from CMS in `Admin Panel` > `Integrations` > `Discord` > `Role Mapping`

Here you can view all mapped ranks and what Discord roles they're mapped to, as well as add or delete mappings.

![Sonoran CMS - Discord Role Mapping](getting-started/sonoran-cms-integration/botcms\_rolemap\_1.png)

To add a new mapping, first start by selecting a rank:

![Sonoran CMS - Discord Role Mapping](getting-started/sonoran-cms-integration/botcms\_rolemap\_2.png)

Next, select the Discord role(s) you wish to map this rank to:

![Sonoran CMS - Discord Role Mapping](getting-started/sonoran-cms-integration/botcms\_rolemap\_3-1.png)

{% hint style="info" %}
**Hint:** You can select multiple roles to map to one rank. However, you can't select multiple ranks at once. Thus, if you want to map multiple ranks to one role, you will have to create a separate entry for every rank you wish to map.
{% endhint %}

When you're ready to create the mapping, click the `Add` button on the right-hand side.

![Sonoran CMS - Discord Role Mapping](getting-started/sonoran-cms-integration/botcms\_rolemap\_4.png)

When you've clicked `Add`, it will show in the list alongside all previously existing mappings.

![Sonoran CMS - Discord Role Mapping](getting-started/sonoran-cms-integration/botcms\_rolemap\_5-1-1.png)

At any time, you can add additional Discord roles to an existing Rank mapping by clicking the plus button.

![Sonoran CMS - Discord Role Mapping](getting-started/sonoran-cms-integration/botcms\_rolemap\_6.png)

This will open up a dropdown where you can select additional Discord roles to map.

![Sonoran CMS - Discord Role Mapping](getting-started/sonoran-cms-integration/botcms\_rolemap\_7-2.png)

When you've selected all desired roles, click outside and it will automatically save your new mapping.

![Sonoran CMS - Discord Role Mapping](getting-started/sonoran-cms-integration/botcms\_rolemap\_8-1.png)

### Role Syncing <a href="#role-syncing" id="role-syncing"></a>

{% hint style="info" %}
Unlike the CAD sync mode, users will not use the `/linkme` command - this is handled within the Sonoran Account SSO.
{% endhint %}

After setting up the above, the command `/sync` will set up everyone's permissions.

Setting the flag `community` to `Yes` will sync your entire community including any linked guilds. Setting it to no or running `/sync` by itself will only sync the server you run it in.

After the initial sync, changes in role mappings will generally sync themselves automatically.

## Features <a href="#features" id="features"></a>

All the below features can be changed through the `/settings` menu described [here](usage/settings.md#cms-settings).

* Sonoran Bot can now ping users on Discord when their form or application statuses are updated in CMS.
* Sonoran Bot syncs calendar events created in your CMS by automatically creating an event in your discord server.
* If enabled, Sonoran Bot syncs the names of your CMS users with their Discord account. Their Discord accounts are automatically given nicknames accordingly.

## Import Discord Roles as CMS Ranks <a href="#import-roles-cms" id="import-roles-cms"></a>

For any Discord guild linked to your CMS, you can choose to import specific roles as ranks into any CMS department.

It will automatically create ranks matching the name and color of your roles, though in depth permission customization will still have to be done as normal.

You can read more on importing Discord roles [here](https://info.sonorancms.com/tutorials/user-management/creating-departments#importing-ranks-from-discord-roles).

![Sonoran CMS - Import Discord Roles as Ranks](getting-started/sonoran-cms-integration/cms\_ranksimportdiscordpanel.png)

## CMS Calendar Integration

If you have linked SonoranBot to your community, creating an event in CMS will automatically create an event within your community's Discord channel making it easy to coordinate community events across multiple platforms!

By clicking the `Interested` button, you will be automatically RSVP'd in CMS.

![Sonoran CMS Calendar Event in Discord](getting-started/sonoran-cms-integration/cms\_calendareventdiscord.png)

## Legacy Role Mapping

You can also set up role mapping directly from Discord, rather than CMS. We generally recommend doing this through CMS as the UI is easier to work with, however we still offer the "legacy" role mapping through Discord as an option.

![Sonoran CMS - Discord-side Role Mapping](getting-started/sonoran-cms-integration/bot\_cmsrolemap01.png)

Select a department, the rank you wish to modify, and the role you wish to apply to the rank.

There will be left and right arrows to page if you have more than 25 roles.

![Sonoran CMS - Discord-side Role Mapping](getting-started/sonoran-cms-integration/bot\_cmsrolemap03.png)

![Sonoran CMS - Discord-side Role Mapping](getting-started/sonoran-cms-integration/bot\_cmsrolemap04.png)

In this example, having `Staff` Role in Discord will get the rank `Civilian Director` in the CMS:

![Sonoran CMS - Discord-side Role Mapping](getting-started/sonoran-cms-integration/bot\_cmsrolemap05.png)

At any time, you can change the dropdowns to select another Department or Rank.

There is ample room for specific customization with role mapping. You can map multiple roles to the same rank and multiple ranks to one role should you so desire.

Keep in mind that sync is bi-directional, so if multiple ranks are mapped to one role (or vice versa) then granting a member one rank will grant them the associated role, which will subsequently grant them the other ranks mapped to the same role.

If you wish to remove a mapping, you can select the Role whose mapping you would like to remove and click the red `Clear Mapping` button.

![Sonoran CMS - Discord-side Role Mapping](getting-started/sonoran-cms-integration/bot\_rolemapclear.png)

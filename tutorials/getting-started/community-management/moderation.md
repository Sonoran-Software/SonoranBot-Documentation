---
title: moderation
description: 
published: true
date: 2023-10-17T23:54:19.970Z
tags: 
editor: markdown
dateCreated: 2023-08-19T00:08:06.914Z
---

# Moderation

## Community Moderation

Using SonoranBot, you have access to several commands that are all logged to a special channel. Keep moderation actions organized and easily control access!

> Moderation commands are available to any Discord server linked to a community, including Free CAD/CMS!
{.is-info}

### Getting Started

#### 1. Set A Logging Channel

You must set a logging channel for any of the commands to work. You can do so with the `/settings` command, first selecting `Logging Settings`, next selecting whether you want to set the "General" or "Moderation" logging channel, then finally selecting what channel that the specified logging will post to.

![bot_setloggingchannel.png](/tutorials/getting-started/community-management/moderation/bot_setloggingchannel.png)

#### 2. Set Permissions

> The permissions in the below table are also what SonoranBot will need to perform them, otherwise you will get an error message.
{.is-warning}


By default, all commands are set to what you expect:

| Command | Required Permission       |
| ------- | ------------------------- |
| `/ban`    | Ban Members               |
| `/kick`   | Kick Members              |
| `/mute`   | Timeout Members           |
| `/warn`   | Manage Guild ("disabled") |

The `/warn` command is attached to Manage Guild by default like all other commands - you will want to give this command to certain roles as desired. This can be accomplished within Discord's Integrations settings (Desktop/Web only).

![bot_discordmanageintegration.png](/tutorials/getting-started/community-management/moderation/bot_discordmanageintegration.png)

![bot_discordintegrationsettings.png](/tutorials/getting-started/community-management/moderation/bot_discordintegrationsettings.png)

Managing integration permissions is outside the scope of this guide, but Discord [has a guide](https://support.discord.com/hc/en-us/articles/4644915651095-Command-Permissions) of their own to walk you through the process. Chances are, you've already done this if you're using the CAD/CMS integrations.

### Usage Examples

When a command is used, a logging entry will be created depending on the action.

#### Ban/Unban

![bot_bancommand.png](/tutorials/getting-started/community-management/moderation/bot_bancommand.png)
![bot_banmessage.png](/tutorials/getting-started/community-management/moderation/bot_banmessage.png)

#### Kick

![bot_kick.png](/tutorials/getting-started/community-management/moderation/bot_kick.png)

#### Mute/Unmute

![bot_mute.png](/tutorials/getting-started/community-management/moderation/bot_mute.png)
![bot_unmute.png](/tutorials/getting-started/community-management/moderation/bot_unmute.png)

#### Warn

![bot_warn.png](/tutorials/getting-started/community-management/moderation/bot_warn.png)
![bot_warnlog.png](/tutorials/getting-started/community-management/moderation/bot_warnlog.png)

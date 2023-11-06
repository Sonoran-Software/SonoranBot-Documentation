---
title: Commands
description: Learn more about Sonoran Bot's Discord commands.
published: true
date: 2023-11-06T23:34:33.355Z
tags: 
editor: markdown
dateCreated: 2023-10-24T20:46:03.525Z
---

# Commands Reference

By default, only server administrators (those with Administrator in the guild) can execute any of the below commands. You must use [Discord's permissions setting feature](https://discord.com/blog/slash-commands-permissions-discord-apps-bots) to give users access.

| Command          | Product | Function                                           |
| ---------------- | ------- | -------------------------------------------------- |
| `/guildlink`     | CAD/CMS | Links a guild to an existing CAD or CMS community  |
| `/rolemap`       | CAD/CMS | Opens role mapping settings                        |
| `/settings`      |         | Allows adjustment of various [settings](https://info.sonoranbot.com/en/tutorials/getting-started/settings) in the bot    |
| `/linkme`        | CAD     | Links your Discord to your SonoranCAD account      |
| `/sync`          | CAD/CMS | Forces a sync with CAD/CMS. If `whole_guild` is toggled, it will force a sync for everyone in your guild, if not then it will only sync you.       |
| `/help`		     	 |				 | Links to sonoranbot.com                            |
| `/clockincms`    | CMS     | Clock in to CMS                                    |
| `/clockoutcms`   | CMS     | Clock out of CMS                                   | 
| `/caduser`       | CAD     | Get information on a linked CAD user               |
| `/embedbuilder`  |         | Possible flags are `link` and `build`              | 
| `/info`          |         | Returns server and community information           |
| `/ping`          |         | Pings the server                                   |
| `/ban`           |         | Ban Members                                        |
| `/unban`         |         | Unban Members                                      |
| `/kick`          |         | Kick Members                                       |
| `/mute`          |         | Timeout Members                                    |
| `/unmute`        |         | Unmute Members                                     |
| `/warn`          |         | Warn Members                                       |

# Deprecated Commands <a href="deprecated-commands" id="deprecated-commands"></a>
These commands are no longer in use, please use the specified replacements (or see notes).
| Command          | Replacement    | Notes                                          |
| ---------------- | -------------- | ---------------------------------------------- |
| `/syncroles`     | `/sync`        | Set `whole_guild` to `Yes` to sync entire guild  |
| `/syncme`        | `/sync`        | Set `whole_guild` to `No` or run `/sync` alone   |
| `/setsyncmode`   | None           | Automatically detects sync mode. If a CMS community has been linked to your guild, then it will sync to that, and and CAD roles will have to be mapped using [CMS -> CAD Permission Sync](https://info.sonorancms.com/integration-capabilities/sonoran-cad-sync)  |
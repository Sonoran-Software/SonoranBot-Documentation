---
description: Sync Sonoran Radio permissions with Discord roles for easy management!
---

# Sonoran Radio Integration

## Sonoran Radio Integration

Use Sonoran Bot to sync Discord roles to SonoranRadio permissions and joinable Radio profiles.

### What this integration does

When a member has mapped Discord roles, the bot converts those roles into:

* A SonoranRadio permission bitmask
* An optional list of Radio profile IDs the member can join

The bot then sends that combined access to SonoranRadio for the linked Sonoran account.

### Requirements

Before setting this up, make sure you have:

1. Sonoran Bot added to your Discord server
2. A SonoranRadio community ID and API key
3. `Manage Server` permission in Discord to configure mappings
4. Linked Sonoran accounts for the members you want to sync

{% hint style="warning" %}
The bot uses the linked Sonoran account for permission sync. If a user is not linked, `/sync` will fail for that user.
{% endhint %}

If you have not added the bot yet, start here:

### Setup

Open `/settings`, then go to the API menu and save your SonoranRadio community ID and API key.

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption><p><code>/settings</code> -> <code>API Menu</code> -> <code>Change Radio Setup</code></p></figcaption></figure>

For general settings navigation, see:

After the Radio credentials are saved, the bot enables one of these sync modes automatically:

* `RADIO` if only Radio is configured
* `CAD_RADIO` if both CAD and Radio are configured
* `CMS_BIDIR` if CMS is configured

{% hint style="info" %}
CMS takes priority over CAD and Radio sync. If CMS credentials are present, live role sync runs through the CMS path until CMS is removed from the community setup.
{% endhint %}

{% hint style="warning" %}
Radio credentials are saved without setup-time validation. The first real validation usually happens when you open the Radio role mapping menu or run `/sync`.
{% endhint %}

### Configure Role Mapping

Run `/rolemap` to configure how Discord roles translate into SonoranRadio access.

If your community is in `CAD_RADIO` mode, the bot first asks whether you want to manage CAD mappings or Radio mappings.

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption><p><code>/rolemap</code> product selector in <code>CAD_RADIO</code> mode</p></figcaption></figure>

If your community is in `RADIO` mode, the bot opens the Radio mapping menu directly.

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption><p><code>/rolemap</code> Radio main menu showing selector</p></figcaption></figure>

#### How a Radio mapping is stored

Each Discord role can store:

* A Radio permission integer
* Zero or more Radio profile IDs

The value is entered as a comma-separated list where:

* The first number is the Radio permission bitmask
* Every number after that is treated as a profile ID

Example:

```
65, 2, 7, 12
```

That means:

* `65` is the Radio permission mask
* `2`, `7`, and `12` are profile IDs the user can join

The bot accepts spaces or commas between values, but the first value must always be the permission mask.

#### Add or change a mapping

1. Run `/rolemap`
2. Select the Discord role you want to map
3. Click `Add Mapping`
4. Enter the Radio permission integer, followed by any optional profile IDs

<div><figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption><p>selected Radio role view in <code>/rolemap</code></p></figcaption></figure> <figure><img src="https://cdn.discordapp.com/attachments/871554360285474847/1509283011722608682/image.png?ex=6a1f3457&#x26;is=6a1de2d7&#x26;hm=f4fe4a1c9d0434151aedf6d0141cd0073e1dea769a86922073ce8348dfa4c41b&#x26;" alt=""><figcaption><p>Radio mapping modal with permission integer and optional profile IDs</p></figcaption></figure></div>

#### Remove a mapping

Enter `0` as the mapping value for that role. The bot treats `0` as delete and removes the stored Radio role map for that Discord role.

### How Sync Works

This is the actual runtime flow used by the bot.

#### 1. The bot finds the member's linked Sonoran account

When a sync starts, the bot looks up the Discord user's linked Sonoran account and gets that account's UUID.

If no linked account is found, the sync stops.

#### 2. The bot checks every Discord server linked to the same community

Radio sync is not limited to the current Discord server.

If you have multiple Discord servers linked to the same Sonoran community, the bot gathers all of them and checks the member's roles across every linked server that the bot is in.

This means the final Radio access is the union of all mapped roles across the whole linked community, not just one guild.

#### 3. The bot converts matched roles into Radio access

For every mapped role the member has:

* The mapping string is parsed
* The permission mask is converted into permission flags
* Any profile IDs in the mapping are collected

Duplicate profile IDs are removed automatically.

#### 4. The bot builds the final SonoranRadio payload

The bot combines all matched mappings into:

* One final permission mask
* One deduplicated list of profile permissions

The profile payload is sent as join access for each collected profile ID.

#### 5. The bot updates SonoranRadio

The bot sends the member's final access to SonoranRadio using the linked Sonoran account UUID.

If the Radio API returns an error, the sync fails and the failure is logged.

### Manual Sync

Members can run `/sync` to force a permission refresh.

{% hint style="info" %}
The Radio sync flow expects the user's Discord account to already be linked to a Sonoran account. The `/linkme` command is only available for CAD-enabled communities and is not part of the Radio-only setup flow.
{% endhint %}

If the community has both CAD and Radio enabled, `/sync` runs both products in the same command. If only Radio is enabled, the success message is Radio-only.

Administrators can also run:

```
/sync community: yes
```

That performs a full community-wide sync for all linked accounts the bot can resolve.

### Automatic Sync

The bot also updates Radio access automatically in these cases:

#### Discord role changes

When a member gains or loses roles, the bot re-checks their role mappings and immediately recalculates their Radio access.

#### Member leaves the server

When a member leaves a linked guild, the bot checks whether that user is still in any other Discord guild linked to the same Sonoran community.

* If they are still in another linked guild, Radio access is left alone
* If they are no longer in any linked guild, the bot clears their Radio access by sending `perm = 0` and an empty profile list

#### Member is banned

The same cleanup logic runs when a member is banned. If that user is no longer in any linked guild for the community, the bot clears their SonoranRadio access.

### Important Behavior

#### CMS overrides CAD/Radio runtime sync

If CMS is configured, the community sync mode becomes `CMS_BIDIR`. CAD and Radio credentials may still remain saved, but runtime role sync stays on the CMS path until CMS is removed.

#### `CAD_RADIO` changes the `/rolemap` experience

If both CAD and Radio are configured, `/rolemap` first shows a product chooser so administrators can open either the CAD mapper or the Radio mapper.

#### Radio mappings are stored per Discord role

Each mapped Discord role stores one raw text value. That value can represent both the permission mask and profile access in one field.

#### Community-wide sync uses all linked guild mappings

This is especially important for networks that run multiple Discord servers for one Sonoran community. A member can inherit Radio access from mapped roles in any linked guild the bot can see.

### Troubleshooting

If Radio sync does not work, check these first:

1. Confirm the user's Sonoran account is linked to Discord
2. Confirm the correct SonoranRadio community ID and API key are saved
3. Confirm the Discord role is actually mapped in `/rolemap`
4. Confirm the permission integer was generated correctly
5. Confirm any profile IDs in the mapping are valid for your Radio setup
6. Run `/sync` manually to test the user

If `/rolemap` or `/sync` fails immediately after setup, the most likely causes are invalid Radio credentials or a missing linked Sonoran account.

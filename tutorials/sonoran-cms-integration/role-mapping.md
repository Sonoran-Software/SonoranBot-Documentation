---
description: Learn more about mapping Discord roles in Sonoran CMS!
---

# Role Mapping

## Mapping Discord Roles and CMS Ranks

In the `Administration` panel of the CMS, navigate to `Integrations` > `Discord` > `Role Mapping`

Here, you can configure your CMS x Discord Mappings.

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

## Bi-Directional Mapping

The bi-directional mapping allows a CMS rank to be synced to one or more Discord roles.\
If a user gets _any_ piece of the mapping (the CMS rank or any of the Discord roles) they will automatically recieve the _entire_ mapping.

In this example, the `Bronze VIP` CMS rank is mapped to a `Bronze VIP` role in two different Discords.

### Use Case:

Bi-directional is best for one-to-one mapping of a CMS rank to a matching Discord role in one or more Guilds.

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

### CMS Actions:

* Adding this CMS rank to the user will grant all mapped Discord roles.
* Removing this CMS rank from the user will remove all mapped Discord roles.

### Discord Actions:

* Adding one of these Discord roles will add both the CMS rank, and any remaining Discord roles.
* Removing one of the Discord roles will remove the CMS rank, and any remaining Discord roles.
* Running a `/sync` will add any missing pieces of this mapping to the user, as long as they have part of it.

## Dependency Role

The dependency role mapping grants a Discord role for having one or more of the CMS ranks.\
Granting or removing the Discord role will do nothing.

### Use Case:

Dependency role mappings are useful for organizing multiple CMS ranks under a higher-level Discord role for better labeling and visualization.

For example, if you have various administration ranks, you can assign the `Staff` Discord role to anyone holding one of these individual ranks. This way, the `Staff` role serves as a visual organizer without the `Staff` role itself granting all the underlying CMS ranks (`Admin`, `Moderator`, etc.) as it would with a [bi-directional mapping](role-mapping.md#bi-directional-mapping).

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

### CMS Actions:

* Adding any one of the CMS ranks to the user will grant the Discord role.
* Removing all of the CMS ranks from the user will remove the Discord role.

### Discord Actions:

* Adding the Discord role will have no impact.
* Removing the Discord role will have no impact.
* Running a `/sync` will add the Discord role if the user has at least one of the CMS ranks.

## Example of Both Types

Both [bi-directional](role-mapping.md#bi-directional-mapping) and [dependent role](role-mapping.md#dependency-role) mappings can be used at the same time.

**Use Case:**

1. I want to grant each administrative rank in the CMS (`moderator`, `admin`, etc.) an associated Discord role (`moderator`, `admin`, etc.).
2. I also want everyone who has one of those administrative ranks to also have the general `Staff` Discord role.

#### Steps:

**Bi-Directional Mapping:**

1. Create a bi-directional mapping for each administrative rank to its associated Discord role:
   * Sync the `Admin` CMS rank with the `Admin` Discord role.
   * Sync the `Moderator` CMS rank with the `Moderator` Discord role.
   * Sync the `Super Admin` CMS rank with the `Super Admin` Discord role.
   * Sync the `Manager` CMS rank with the `Manager` Discord role.

**Dependency Mapping:**

2. Create a dependency mapping from every administrative rank in the CMS (`moderator`, `admin`, etc.) to the `Staff` Discord role:
   * This grants the `Staff` Discord role if the user has either the `Admin`, `Moderator`, `Super Admin`, or `Manager` CMS rank(s).

**Note:** I do _NOT_ add the `Staff` Discord role to every bi-directional mapping, as granting the user the `Staff` Discord role would then grant every remaining administrative rank to the user. Remember, if a user has _any_ piece to a bi-directional mapping they will recieve the entire mapping.

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

## Syncing the Role Map

{% hint style="info" %}
After modifying the mapping, your community will automatically be re-synced.\
This may take a couple of minutes to complete.
{% endhint %}

While changes are automatic, you can also manually re-sync users with the `/sync` command.

Setting the flag `community` to `Yes` will sync your entire community including any linked guilds. Setting it to no or running `/sync` by itself will only sync the server you run it in.

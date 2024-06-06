---
description: Learn more about mapping Discord roles in Sonoran CMS!
---

# Role Mapping

## Mapping Discord Roles and CMS Ranks

In the `Administration` panel of the CMS, navigate to `Integrations` > `Discord` > `Role Mapping`

Here, you can configure your CMS x Discord Mappings.

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

## Bi-Directional Mapping

The bi-directional mapping allows a CMS rank to be synced to one or more Discord roles.

In this example, the `Bronze VIP` CMS rank is mapped to a `Bronze VIP` role in two different Discords.

### Use Case:

Bi-directional is best for one-to-one mapping of a CMS rank to a matching Discord role in one or more Guilds.

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

### CMS Actions:

* Adding this CMS rank to the user will grant both Discord roles.
* Removing this CMS rank from the user will remove both Discord roles.

### Discord Actions:

* Adding one of these Discord roles will add both the CMS rank, and any remaining Discord roles.
* Removing one of the Discord roles will remove the CMS rank, and any remaining Discord roles.
* Running a `/sync` will add any missing pieces of this mapping to the user, as long as they have part of it.

## Dependency Role

The dependency role mapping allows a user to recieve a Discord role based on having at least one of the required CMS ranks.

### Use Case:

Dependency role mappings are best for categorizing multiple CMS ranks with a higher level Discord role.

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

### CMS Actions:

* Adding any one of the CMS ranks to the user will grant the Discord role.
* Removing all of the CMS ranks from the user will remove the Discord role.

### Discord Actions:

* Adding the Discord role will have no impact.
* Removing the Discord role will have no impact.
* Running a `/sync` will add the Discord role if the user has at least one of the CMS ranks.

## Example of Both Types

Both bi-directional and dependent role mappings can be used at the same time.

#### Bi-Directional

* Sync the `Admin` CMS rank with the `Admin` Discord role
* Sync the `Moderator` CMS rank with the `Moderator` Discord role
* Sync the `Super Admin` CMS rank with the `Super Admin` Discord role
* Sync the `Manager` CMS rank with the `Manager` Discord role

#### **Dependent Role**

* Grant the `Staff` Discord role if the user has either the `Admin`, `Moderator`, `Super Admin`, or `Manager` CMS rank(s).

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

## Syncing the Role Map

{% hint style="info" %}
After modifying the mapping, your community will automatically be re-synced.\
This may take a couple of minutes to complete.
{% endhint %}

While changes are automatic, you can also manually re-sync users with the `/sync` command.

Setting the flag `community` to `Yes` will sync your entire community including any linked guilds. Setting it to no or running `/sync` by itself will only sync the server you run it in.

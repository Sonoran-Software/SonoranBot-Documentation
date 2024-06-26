---
description: Learn more about mapping Discord roles in Sonoran CMS!
---

# Role Mapping

## Mapping Discord Roles and CMS Ranks

In the `Administration` panel of the CMS, navigate to `Integrations` > `Discord` > `Role Mapping`

Here, you can configure your CMS x Discord Mappings.

## Example Mapping

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

### **Use Case:**

1. I want to grant each administrative rank in the CMS (`moderator`, `admin`, etc.) an associated Discord role (`moderator`, `admin`, etc.).
2. I also want everyone who has one of those administrative ranks to also have the general `Staff` Discord role.

### Steps:

#### ➡️**Mapping:**

1. Create a mapping from every administrative rank in the CMS (`moderator`, `admin`, etc.) to the `Staff` Discord role:

* This grants the `Staff` Discord role if the user has either the `Admin`, `Moderator`, `Super Admin`, or `Manager` CMS rank(s).

#### ⬅️➡️ **Mapping**

2. Create a mapping for each administrative rank to its associated Discord role:

* Sync the `Admin` CMS rank with the `Admin` Discord role.
* Sync the `Moderator` CMS rank with the `Moderator` Discord role.
* Sync the `Super Admin` CMS rank with the `Super Admin` Discord role.
* Sync the `Manager` CMS rank with the `Manager` Discord role.

**Note:** I do _NOT_ add the `Staff` Discord role to every ⬅️➡️ mapping, as granting the user the `Staff` Discord role would then grant every remaining administrative rank to the user.\
Remember, if a user has _any_ piece to a ⬅️➡️ mapping they will receive the entire mapping.

## Syncing the Role Map

{% hint style="info" %}
After modifying the mapping, your community will automatically be re-synced.\
This may take a couple of minutes to complete.
{% endhint %}

While changes are automatic, you can also manually re-sync users with the `/sync` command.

Setting the flag `community` to `Yes` will sync your entire community including any linked guilds. Setting it to no or running `/sync` by itself will only sync the server you run it in.

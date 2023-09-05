---
title: sonoran-cad-integration
description: 
published: true
date: 2023-09-05T18:14:59.271Z
tags: 
editor: markdown
dateCreated: 2023-08-19T00:08:17.845Z
---

# Sonoran CAD Integration

## Manage with Sonoran CMS!

In addition to automatically adding users when applications are accepted, [Sonoran CMS](https://info.sonorancms.com/why-choose-sonoran-cms/why-choose-sonoran-cms) can also manage your community's CAD permissions!

[Learn more today!](https://info.sonorancms.com/why-choose-sonoran-cms/why-choose-sonoran-cms)

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-M4pGN81fb4R6zFhodcu%2Fuploads%2FSjLVb2jKeswR4am8X9kH%2FBigSquare.png?alt=media&#x26;token=4e641634-cc44-44cf-b1c3-20ca4f746c89" alt=""><figcaption><p>Sonoran CMS x Sonoran CAD</p></figcaption></figure>

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-M4pGN81fb4R6zFhodcu%2Fuploads%2Fv9ymIkkSomDZc27026rG%2Fimage.png?alt=media&#x26;token=5f470a38-3187-4394-9f18-5ed3cdf44603" alt=""><figcaption></figcaption></figure>

## Sonoran CAD Integration Guide

### Setup Guide

https://www.youtube.com/watch?v=VATCtHH7GQw

### Permissions Synchronization - CAD

> You must have the Manage Server permission on the Discord server in order to set up this process.
{.is-warning}

The bot provides a brand new menu to assist you with assigning roles to permissions.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-M4pGN81fb4R6zFhodcu%2Fuploads%2FXPqaE0G5eS0lR7prLghk%2FScreenshot_13.png?alt=media&#x26;token=f775bc57-30c5-42ff-8e96-c7fecbac5069" alt=""><figcaption></figcaption></figure>

Select a role:

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-M4pGN81fb4R6zFhodcu%2Fuploads%2FWMeVXTTMK6t0ANIWIrfy%2FScreenshot_14.png?alt=media&#x26;token=7af69b0e-a0cd-41cb-8bd3-6dc8591a5861" alt=""><figcaption></figcaption></figure>

Clicking "Set Mapping" will present an option to specify a code (using the linked tool) or an existing permission key. Enter "0" as the permission mask to delete the current mapping instead.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-M4pGN81fb4R6zFhodcu%2Fuploads%2F9cCEioESKYGzwVV9SJEy%2FScreenshot_15.png?alt=media&#x26;token=1f53749a-423a-4da3-a207-3bc4343e174c" alt=""><figcaption></figcaption></figure>

Successfully entering this information will bring you back to the main role mapping screen with the new permission set.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-M4pGN81fb4R6zFhodcu%2Fuploads%2FXkCTGkMTSZvbgKkk1TBb%2FScreenshot_16.png?alt=media&#x26;token=594526fe-cc43-449f-8c43-d075cdca14dd" alt=""><figcaption></figcaption></figure>

### User Setup

1. Every user in the Discord will get their [Secret ID from their Settings page](https://info.sonorancad.com/sonoran-cad/api-integration/getting-started/account-secret-id).
2. Every user in the Discord will then use `/linkme <secretid>` to link their Sonoran CAD account to their current Discord account. This will automatically populate their API ID.
3. Community members can use the `/syncme` command in Discord to force a permissions sync.
4. Communities should **no longer use public permission keys in the CAD**, as the bot will automatically remove CAD permissions from users if they don't have a Discord role for it.

Now, whenever a role is added or removed, the bot will automatically update the user's permissions to match! If the user ever leaves the server, the bot will immediately remove all permissions from their account, although they will still be in the community.

### Changing your Account Secret ID

Sometimes, you may wish to change your secret ID. If you do so from the [Settings page](https://info.sonorancad.com/sonoran-cad/api-integration/getting-started/account-secret-id), you must use the `/changesecret <new key>` command or the bot will remove all your permissions on Sonoran CAD (if the optional security setting below is enabled).

### Optional Security Setting

By default, the bot will not remove permissions from users who do not have a matching secret key to their Discord ID. This can be enabled by setting `stripUnmappedUsers` to true with the `s!setting` command.

### Best Practices and FAQ

* It is advised to not sync potentially dangerous permissions (such as Admin Access permissions) with Discord roles **unless** you trust staff with that role, or it's just you.
* The community owner is completely ignored during the synchronization process.
* "Principle of Least Privilege" should be exercised during this setup. Don't give out permissions you don't think users performing the role would need.
* Discontinue use of permission keys ASAP. The bot "takes over" synchronization and will remove permissions granted by permission keys if they don't have a role that grants it.
  * Same goes for manual permission grants, **unless there is no role granting that permission**.


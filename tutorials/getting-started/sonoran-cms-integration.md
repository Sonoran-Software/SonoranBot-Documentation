---
title: Sonoran CMS Integration
description: Link Sonoran Bot to Sonoran CMS for role syncing and other handy features!
published: true
date: 2023-09-27T19:32:46.548Z
tags: 
editor: markdown
dateCreated: 2023-08-19T00:08:23.412Z
---

# Video Guide

Sync your Discord roles with SonoranCMS permissions!

https://www.youtube.com/watch?v=mlH4TlybT_4

# Getting Started <a href="#getting-started" id="getting-started"></a>

By default, **only Administrators of the Discord guild can access the commands** below. These can be changed in the Settings menu of the server.

## 1. Discord SSO Linking <a href="#1.-discord-sso-linking" id="1.-discord-sso-linking"></a>

Users must link their Discord to their Sonoran account. This will also automatically add their Discord [API ID](https://info.sonorancms.com/developer-api-documentation/api-integration/getting-started/api-id-system).

**Enable Discord Sync**

* In the Administration panel select `Advanced` -> `Integrations` -> `Discord`
* Toggle the `Discord Bot Integration` box

<figure><img src="https://1004916355-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MdBOa9OFjtdqw9FdXli%2Fuploads%2FzxvTfLFdaeS9Gs1NVvt5%2FCMS_DiscodIntegrationCircle.png?alt=media&#x26;token=3f9bd71d-098e-47e9-a5cd-6ba0943a6334" alt=""><figcaption><p>Sonoran CMS - Enable Discord Bot</p></figcaption></figure>

**Link your Discord Account**

Once enabled in the CMS, users who do not yet have their Discord account linked with their Sonoran account will see the following banner:

<figure><img src="https://1004916355-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MdBOa9OFjtdqw9FdXli%2Fuploads%2FvuBlorebVznW98h1ebyK%2FScreen%20Shot%202023-01-08%20at%2012.04.00%20PM.png?alt=media&#x26;token=2a1b84bb-e963-4b18-9b16-a13970ed0603" alt=""><figcaption><p>Sonoran CMS - Link Your Discord Account​</p></figcaption></figure>

## 2. Role Mapping <a href="#2.-role-mapping" id="2.-role-mapping"></a>

The command `/rolemap` can now be used.

The following image is when a CMS mode is selected.

<figure><img src="https://1004916355-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MdBOa9OFjtdqw9FdXli%2Fuploads%2FyLHpmpmWQSVsGbqEUlsX%2FScreenshot_5.png?alt=media&#x26;token=8a6a322f-ab7f-4ad2-9c91-ee24e05fee17" alt=""><figcaption><p>Options when set to CMS</p></figcaption></figure>

Select a department, rank you wish to modify, and the role you wish to apply to the rank.

<figure><img src="https://1004916355-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MdBOa9OFjtdqw9FdXli%2Fuploads%2FE4hxs6VNQbxUpj63flcA%2FScreenshot_6.png?alt=media&#x26;token=cc6b1c94-f258-4649-9131-b85b4362dd9c" alt=""><figcaption></figcaption></figure>

The "Set Department-wide Role" button will automatically assign the Department (in this example, Community Leadership) to anyone with the role you select.

<figure><img src="https://1004916355-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MdBOa9OFjtdqw9FdXli%2Fuploads%2FF7XkBI6psusjcRz5Kf3S%2FScreenshot_7.png?alt=media&#x26;token=cab4d47d-bee4-4141-a38f-e03e48be9d80" alt=""><figcaption><p>Click "Select Roles"</p></figcaption></figure>

Use the left and right arrows to page if you have more than 25 roles.

<figure><img src="https://1004916355-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MdBOa9OFjtdqw9FdXli%2Fuploads%2Fwv61embWIghD3fquhlh9%2FScreenshot_12.png?alt=media&#x26;token=cfe5563e-7135-4393-b336-85279addcaf5" alt=""><figcaption><p>Use the left and right arrows to page if you have more than 25 roles.</p></figcaption></figure>

<figure><img src="https://1004916355-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MdBOa9OFjtdqw9FdXli%2Fuploads%2F7qnoP8tV0c9NbTjmOQ72%2FScreenshot_8.png?alt=media&#x26;token=5dcdf53e-0da7-4bda-85c1-45f7774a8e29" alt=""><figcaption></figcaption></figure>

The "Staff Role" will get the rank "Director" in the CMS.

This is only an example! At any time, you can change the dropdowns to select another Department or Rank.

# Role Syncing <a href="#role-syncing" id="role-syncing"></a>

> Unlike the CAD sync mode, users will not use the `/linkme` command - this is handled within the Sonoran Account SSO.
{.is-info}

After setting up the above, the command `/syncroles` will set up everyone's permissions.

# 🛠 Getting Started

Sonoran Bot supports either CAD or CMS syncing. The below tutorial applies to both syncing methods; afterwards, follow the appropriate link to set up the syncing you wish to use.

{% hint style="warning" %}
All commands require at least the Manage Server permission on the Discord server you are running the commands in. You will also need a number of other permissions upon inviting the bot.
{% endhint %}

### 1. Invite the Bot to Your Server

[Invite the bot to your Discord server](https://discord.com/api/oauth2/authorize?client\_id=1060274480930361424\&permissions=9395244032\&scope=bot%20applications.commands). You must have the "Manage Server" permission to add bots; plus any permissions the bot requires to function.

### 2. Run the Setup Command

1. After inviting the bot, run the `/setup` command.
2.  Determine which syncing method you wish to use; you may set up both community types.

    1. Enter your [Sonoran CAD ID and API key](https://info.sonorancad.com/sonoran-cad/api-integration/getting-started/retrieving-your-credentials).
    2. AND/OR Enter your [Sonoran CMS ID and API key](https://info.sonorancms.com/developer-api-documentation/api-integration/getting-started#gather-your-credentials).



    <figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption><p>Enter the information needed above.</p></figcaption></figure>

    You will then be presented with the results of the setup.

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
If you set up both CMS and CAD, the Discord bot will automatically use CMS mode. Otherwise, it will use the successfully set up mode.
{% endhint %}

### 3. Invite to Additional Servers

If your community uses multiple discord servers, you can link them all to the same community to utilize the permissions sync easily using the `/guildlink` command, as shown below.

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

Fill out the information (using either your CAD or CMS information), and you will receive a confirmation. At this point, you can use the other commands just like on the primary server.

### 4. Set up Integrations

At this point, you will need to select either CAD or CMS integration. We highly encourage users to make use of the CMS integration as the CMS can integrate with the CAD on its own!

{% content-ref url="sonoran-cms-integration.md" %}
[sonoran-cms-integration.md](sonoran-cms-integration.md)
{% endcontent-ref %}

{% content-ref url="sonoran-cad-integration.md" %}
[sonoran-cad-integration.md](sonoran-cad-integration.md)
{% endcontent-ref %}

{% content-ref url="community-management/" %}
[community-management](community-management/)
{% endcontent-ref %}

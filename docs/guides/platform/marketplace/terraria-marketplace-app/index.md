---
slug: terraria-marketplace-app
author:
  name: Linode Community
  email: docs@linode.com
description: "Deploy a Terraria server on Linode using Marketplace Apps."
keywords: ['terraria','marketplace app', 'game server']
license: '[CC BY-ND 4.0](https://creativecommons.org/licenses/by-nd/4.0)'
published: 2019-04-05
modified: 2021-09-16
modified_by:
  name: Linode
title: "Deploying Terraria through the Linode Marketplace"
contributor:
  name: Linode
external_resources:
 - '[The Official Terraria Wiki](https://terraria.gamepedia.com/Terraria_Wiki)'
tags: ["linode platform","marketplace","cloud-manager"]
aliases: ['/platform/marketplace/deploying-terraria-with-marketplace-apps/', '/platform/one-click/deploying-terraria-with-one-click-apps/','/guides/deploying-terraria-with-one-click-apps/','/guides/deploying-terraria-with-marketplace-apps/']
---

Terraria is a two-dimensional sandbox game in which players explore the world, collect resources, build structures, and battle enemies in procedurally generated environments. In Terraria a player begins by digging for ore, and the further they dig the more adventure they find. Multiplayer mode can be either cooperative or PvP.

Hosting your own Terraria server gives you control over the world, the players, and the objectives. Your world, your rules.

## Deploying the Terraria Marketplace App

{{< content "deploy-marketplace-apps-shortguide">}}

**Software installation should complete within 5-15 minutes after the Linode has finished provisioning.**

## Configuration Options

### Terraria Options

You can configure your Terraria Marketplace App by providing values for the following fields:

| **Field** | **Description** |
|-----------|-----------------|
| **Steam Username** | Your [Steam username](https://store.steampowered.com). [Steam Guard](https://support.steampowered.com/kb_article.php?ref=4020-ALZM-5519) must be turned off. *Required*. |
| **Steam Password** | Your Steam password. *Required*. |
| **World Name** | The name of the Terraria virtual [world](https://terraria.gamepedia.com/World). *Advanced Configuration*. |
| **Server Password** | The server's password, if you would like to make the server password protected. *Advanced Configuration*. |
| **Message of the Day** | The message of the day text that is displayed whenever a player logs on to the server. *Advanced Configuration*. |
| **Difficulty Level** | The world difficulty level. *Advanced Configuration*. |
| **Maximum Players** | The maximum amount of players allowed on the server. A number from 1-255. *Advanced Configuration*. |
| **Port** | The port number that the game server listens on. *Advanced Configuration*. |
| **Seed** | A [random seed](https://terraria.gamepedia.com/World_Seed) used by the world generation algorithm to create a unique world. For example: `qazwsx123`. *Advanced Configuration*. |

### General Options

For advice on filling out the remaining options on the **Create a Linode** form, see [Getting Started > Create a Linode](/docs/guides/getting-started/#create-a-linode). That said, some options may be limited or recommended based on this Marketplace App:

- **Supported distributions:** Debian 9
- **Recommended minimum plan:** 8GB Dedicated CPU or Shared Compute Instance

## Getting Started after Deployment

After Terraria has finished installing, you will be able to access your server by copying your Linode's IPv4 address from the [Linode Cloud Manager](https://cloud.linode.com) and then connecting to it within the game.

{{< caution >}}
You must disable Steam Guard to connect to your Terraria server. If you don't disable Steam Guard, you may be locked out of your account and will need to reset your password. To disable Steam Guard, navigate to the Steam Preferences menu, then open the **Account** pane. Click on **Manage Steam Guard Account Security**, then click on **Turn Steam Guard off**.
{{</ caution >}}

To find your Linode's IPv4 address and connect to it:

1. Click on the **Linodes** link in the sidebar. You will see a list of all your Linodes.

2. Find the Linode you just created when deploying your app and select it.

3. Navigate to the **Networking** tab.

4. Your IPv4 address will be listed under the **Address** column in the **IPv4** table.

5. Copy the IPv4 address.

6. Open Terraria, then click **Multiplayer**.

7. Click on **Join via IP**.

8. You will be prompted to select a character, or create a new one if you don't have any characters. Select or create a character.

9. Type in your IP address, then click **Accept**.

    ![Enter your Linode's IP address.](terraria-marketplace-enter-ip.png)

10. You will be prompted to enter in your Terraria Marketplace App's port. If you did not specify a different port in the advanced configuration section, use port 7777. Click **Accept**.

    ![Enter the Terraria server's port](terraria-marketplace-enter-port.png)

    You will be connected to the server.

## Software Included

The Terraria Marketplace App will install the following required software on your Linode:

| **Software** | **Description** |
|--------------|-----------------|
| [**Terraria**](https://terraria.org) | Game server. |
| [**LinuxGSM**](https://linuxgsm.com) | A command line tool for the deployment and management of Linux game servers. |
| [**UFW**](https://wiki.ubuntu.com/UncomplicatedFirewall) | Firewall utility. Port 7777, unless otherwise specified, will allow outgoing and incoming tcp and udp traffic. |
| [**Fail2ban**](https://www.fail2ban.org/wiki/index.php/Main_Page) | Fail2Ban is an intrusion prevention software framework that protects computer servers from brute-force attacks. |

{{< content "marketplace-update-note-shortguide">}}

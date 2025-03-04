---
slug: serverwand-marketplace-app
author:
  name: Linode
  email: docs@linode.com
description: "ServerWand is a magical control panel for managing websites and servers. Learn how to deploy ServerWand on Linode using Marketplace Apps."
keywords: [ 'serverwand','marketplace','control panel','hosting']
tags: ["cloud manager","linode platform", "marketplace"]
license: '[CC BY-ND 4.0](https://creativecommons.org/licenses/by-nd/4.0)'
published: 2021-02-23
modified: 2021-09-16
modified_by:
  name: Linode
title: "Deploying ServerWand through the Linode Marketplace"
contributor:
  name: Linode
external_resources:
- '[ServerWand Pricing](https://serverwand.com/pricing)'
- '[ServerWand Documentation](https://serverwand.com/docs/)'
- '[ServerWand Blog](https://serverwand.com/blog/)'
aliases: ['/platform/marketplace/deploy-serverwand-with-marketplace-apps/', '/platform/one-click/deploy-serverwand-with-one-click-apps/','/guides/deploy-serverwand-with-one-click-apps/','/guides/deploy-serverwand-with-marketplace-apps/']
---

[ServerWand](https://serverwand.com) is a magical control panel for managing websites and servers. Host multiple sites on a single server, manage apps, firewall, databases, backups, system users, cron jobs, SSL, and email with an intuitive interface.

## Deploying the ServerWand Marketplace App

{{< content deploy-marketplace-apps-shortguide >}}

**Software installation should complete within 2-5 minutes after the Linode has finished provisioning.**

## Configuration Options

For advice on filling out the remaining options on the **Create a Linode** form, see [Getting Started > Create a Linode](/docs/guides/getting-started/#create-a-linode). That said, some options may be limited or recommended based on this Marketplace App:

- **Supported distributions:** Ubuntu 18.04 LTS
- **Recommended minimum plan:** All plan types and sizes can be used.

## Getting Started After Deployment

Once your ServerWand is up and running, you can connect it to your ServerWand account and manage it through the ServerWand control panel.

### Connect your Linode to ServerWand

1. Register or Sign in to the [ServerWand Control Panel](https://manage.serverwand.com/).

1. Click the **Create** button and select **Server**.

    ![Create a ServerWand Server](create-serverwand-server.png "Create a ServerWand Server")

1. On the Server details page, click **Choose** and then select **Linode**.

1. When prompted for access permissions, click **Accept and Continue**.

    ![Accept Linode Access Permissions](accept-permissions.png "Accept Linode Access Permissions")

1. After returning to ServerWand, select your Linode from the **Server** dropdown menu.

1. Give your server a name and click **Save**.

1. ServerWand will connect to your Linode and install all the necessary software so that it can then be managed in ServerWand.

{{< content "marketplace-update-note-shortguide">}}

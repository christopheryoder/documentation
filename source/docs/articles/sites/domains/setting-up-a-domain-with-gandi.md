---
title: Setting Up a Domain with Gandi
description: Learn how to edit a domain's Zone Record in Gandi so that it resolves to your Pantheon site.
category:
  - going-live
keywords: dns, dns records, point your domain, point domain to pantheon, pointing your domain to your pantheon site, dns host, dns configuration, add domain to a site, gandi, point gandi domain to pantheon, redirect gandi domain to pantheon, gandi domain dns, zone, zone record, gandi zone record, dns zones
---
This article assumes that you have already purchased a domain from Gandi.

## Setting Up the Zone Record
In order to get your domain resolving to your Pantheon site, you will need to edit and associate a Zone Record with the domain in the Gandi domain administration panel.

First, navigate to the DNS Zones panel and click the **DNS ZONES** button above the domains list.

![](/source/docs/assets/images/desk_images/197253.png)

From the Zones panel, select the file that you will use for your domain. If one does not yet exist, create a new Zone file.

Click the **Zone file** in the list to start editing.

Change the editing mode to "Expert" in the dropdown menu on the right.

**Note**: If you are editing a pre-existing Zone file, you will receive a notice (see image below, the notice is highlighted) that tells you that the zone file is currently being used and you will need to create a new version.

![Configure the A records](/source/docs/assets/images/desk_images/197261.png)

The zone configuration in the above example is as folllows:

    pantheonsupport.com 10800 IN A 192.237.142.203
    www 10800 IN CNAME pantheonsupport.com

In line 1, we have an A Record in place for our bare domain (ie "pantheonsupport.com"):

    pantheonsupport.com 10800 IN A 192.237.142.203

In line 2, we have a CNAME in place to accomodate 'www':

    www 10800 IN CNAME pantheonsupport.com

When you have entered your configuration (and double-checked that it is correct twice!), click the **Use Version** button. If you've followed the steps in this article, your DNS configuration for your new domain is now complete on the Gandi end.

## Add Your Domain to Pantheon

In order for your domain to resolve to your Pantheon site, it will need to be added to your sites Pantheon dashboard. See [Going Live](/docs/articles/going-live) for more details.

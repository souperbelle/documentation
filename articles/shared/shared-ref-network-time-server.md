---
title: Network Time Protocol server access
description: This guide shows you how to configure access to the Network Time Protocol (NTP) server
services: shared-services
author: shighmoor
reviewer: shighmoor
lastreviewed: 06/11/2020
toc_rootlink: Reference
toc_sub1: 
toc_sub2:
toc_sub3:
toc_sub4:
toc_title: Network Time Protocol server access
toc_fullpath: Reference/shared-ref-network-time-server.md
toc_mdlink: shared-ref-network-time-server.md
---

# Network Time Server access

The UKCloud Network Time Protocol (NTP) server is available for use by UKCloud's customers. It is available in both the Assured OFFICIAL and Elevated OFFICIAL security domains.

## Assured OFFICIAL Platform

Update the NTP server of your Assured virtual machines with one or both of the following IP addresses:

`37.26.90.192`

`37.26.94.232`

## Elevated OFFICIAL Platform

Update the NTP server of your Elevated virtual machines with one or both of the following IP addresses:

`x.y.89.96`

`x.y.93.144`

Replace `x.y` with the first two octets of the Elevated OFFICIAL public IP addresses. If you are unsure of these, contact UKCloud Support.

You may need to adjust your firewall and NAT rules to allow communication between the NTP server of your virtual machines and the UKCloud network time server.

## Feedback

If you find a problem with this article, click **Improve this Doc** to make the change yourself or raise an [issue](https://github.com/UKCloud/documentation/issues) in GitHub. If you have an idea for how we could improve any of our services, send an email to <feedback@ukcloud.com>.

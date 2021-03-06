---
title: How to create an isolated VDC network
description: Shows how to create an isolated VDC network within the VMware Cloud Director/vCloud Director Tenant Portal
services: vmware
author: shighmoor
reviewer: shighmoor
lastreviewed: 14/09/2020

toc_rootlink: How To
toc_sub1:
toc_sub2:
toc_sub3:
toc_sub4:
toc_title: Create an isolated VDC network
toc_fullpath: How To/vmw-how-create-isolated-network.md
toc_mdlink: vmw-how-create-isolated-network.md
---

# How to create an isolated VDC network

## Overview

An organisation virtual data centre network enables its virtual machines (VMs) to communicate with each other or to provide access to external networks. A single VDC can have multiple networks.

There are two network flavours, isolated and routed:

- An isolated (internally connected) network is one that only VMs within the VDC can connect to. This article describes how to create an isolated VDC network.

- A routed network (externally connected) provides access to machines and networks outside the VDC via the edge gateway. You can have up to nine usable routed networks per VDC. Creation of routed networks is described in [*How to create a routed VDC network*](vmw-how-create-routed-network.md).

## Creating an isolated network

### [VMware Cloud Director 10.1](#tab/tabid-a)

1. In the VMware Cloud Director *Virtual Data Center* dashboard, select the VDC in which you want to create the network.

2. In the left navigation panel, under *Networking*, select **Networks**.

    ![Networks tab in VMware Cloud Director](images/vmw-vcd10.1-tab-networks.png)

3. Click **New**.

    ![Add network button](images/vmw-vcd10.1-btn-new-network.png)

4. On the *Network Type* page of the *New Organization VDC Network* dialog box, select **Isolated**, then click **Next**.

    ![New Organization VDC Network dialog box - Network Type page - Isolated network](images/vmw-vcd10.1-new-network-isolated.png)

5. On the *General* page:

    - Enter a **Name** and **Description** for the network.

    - In the **Gateway CIDR** field, enter the gateway address for the network.

    - Select the **Shared** option to make the network available to other VDCs within the same organisation.

    ![New Organization VDC Network dialog box - General page](images/vmw-vcd10.1-new-network-general.png)

6. Click **Next**.

7. On the *Static IP Pools* page, in the **Static IP Pools** field, enter a range of addresses to be consumed by the VMs connecting to the network, then click **Add**.

    As an example, if you give the gateway address as `192.168.1.1/24`, you may then want to create a **Static IP Pool** of `192.168.1.10-192.168.1.100`. This will give you a pool of 91 IP addresses to assign to machines within your network. You can always increase this later if needed.

    You can add multiple IP pools.

    ![New Organization VDC Network dialog box - Static IP Pools page](images/vmw-vcd10.1-new-network-ip-pool.png)

8. Click **Next**.

9. On the *DNS* page, enter DNS information if possible.

    ![New Organization VDC Network dialog box - DNS page](images/vmw-vcd10.1-new-network-dns.png)

10. Click **Next**.

11. On the *Ready to Complete* page, review your selections then click **Finish**.

### [vCloud Director 9.7](#tab/tabid-b)

1. In the vCloud Director *Virtual Datacenters* dashboard, select the VDC in which you want to create the network.

2. In the left navigation panel, select **Networks**.

    ![Networks tab in vCloud Director](images/vmw-vcd-tab-networks.png)

3. Click **Add**.

    ![Add network button](images/vmw-vcd-btn-add-network.png)

4. In the *Network Type* page of the *New Organization VDC Network* dialog box, select **Isolated** then click **Next**.

    ![New Organization VDC Network dialog box - Network Type - Isolated](images/vmw-vcd-add-network-isolated.png)

5. In the *General* page, enter a **Name** and **Description** for the network.

6. In the **Gateway CIDR** field, the gateway address for the network.

7. Select the **Shared** option to make the network available to other VDCs within the same organisation.

    ![New Organization VDC Network dialog box - General](images/vmw-vcd-add-network-general.png)

8. Click **Next**.

9. In the **Static IP Pools** field, enter a range of addresses to be consumed by the VMs connecting to the network, then click **Add**.

    As an example, if you give the gateway address as `192.168.1.1/24`, you may then want to create a **Static IP Pool** of `192.168.1.10-192.168.1.100`. This will give you a pool of 91 IP addresses to assign to machines within your network. You can always increase this later if needed.

    You can add multiple IP pools.

    ![New Organization VDC Network dialog box - Static IP Pools](images/vmw-vcd-add-network-ip-pool.png)

10. When you're done, click **Next**.

11. In the *DNS* page, enter DNS information if possible then click **Next**.

    ![New Organization VDC Network dialog box - DNS](images/vmw-vcd-add-network-dns.png)

12. On the *Ready to Complete* page, review your selections then click **Finish**.

***

## Next steps

Now you've created your network to connect your VDC with the outside world, may want to configure your edge gateway to control what traffic is allowed into and out of your VDC. You may also want to start building some VMs. For a walkthrough on how to do this, see [*How to build a virtual machine with UKCloud for VMware*](vmw-gs-build-vm-vcd.md).

## Feedback

If you find a problem with this article, click **Improve this Doc** to make the change yourself or raise an [issue](https://github.com/UKCloud/documentation/issues) in GitHub. If you have an idea for how we could improve any of our services, send an email to <feedback@ukcloud.com>.

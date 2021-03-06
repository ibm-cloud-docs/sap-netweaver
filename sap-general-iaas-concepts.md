---

copyright:
  years: 2017, 2020
lastupdated: "2020-04-17"

keywords: SAP NetWeaver, {{site.data.keyword.cloud_notm}}, data centers, {{site.data.keyword.baremetal_short}}, deployment, VLANs, SAP Certified, database

subcollection: sap-netweaver

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# SAP NetWeaver on IBM Cloud IaaS Overview
{: #sap-netweaver-on-ibm-cloud-iaas-overview}

An Infrastructure-as-a-server (IaaS) environment consists of many components: data center, compute, connectivity, storage, and network.
{:shortdesc}

## Data centers
{: #data-centers}

With data centers across North and South America, Europe, Asia, and Australia, you can provision cloud resources where (and when) you need them. Each data center is connected to the {{site.data.keyword.cloud_notm}} global private network, making data transfers faster and more efficient anywhere in the world.

[View the network map](https://www.ibm.com/cloud/data-centers/){: external} for more information on the {{site.data.keyword.cloud_notm}} data centers and points of presence (PoPs).

## Bare metal servers
{: #bare-metal-servers}

{{site.data.keyword.baremetal_long}} are physical servers with limited customization capabilities. The servers are dedicated for your use, or your customer's, and not shared in any part, including server resources, with other {{site.data.keyword.cloud_notm}} customers. These servers are managed by you, or your customer, and are provisioned without a hypervisor.

Because customization is limited on bare metal servers, faster provisioning times of between 1 to 4 hours are obtainable. Quick provisioning is helpful when you are trying to get an app to market before the competition.

You are offered an array of RAM and CPU combinations as the SAP-certified servers have a pre-configured amount of RAM and number of CPUs. The combination *cannot* be changed during the ordering process or through a support ticket after servers are deployed.

If your project requires a virtualization layer, the SAP NetWeaver offering includes the option to order {{site.data.keyword.baremetal_short}} that are deployed with VMware ESXi. The ESX instance is under your full control, as it is deployed in your data center. The system is fully configured regarding networking (any further configuration, such as storage, is up to you). It is highly recommended that you have a person with an understanding of ESX administration on staff to successfully start your project.

See [IBM Cloud Bare Metal Servers](https://www.ibm.com/cloud/bare-metal-servers){: external} for more information on bare metal servers.

## Operating systems
{: #operating-systems}

You need to consult [SAP Note 2414097](https://launchpad.support.sap.com/#/notes/2414097){: external} for a list of guest operating systems (OS) to deploy SAP NetWeaver-based systems. An SAP S-user ID is required to access the SAP Note. Licensing for the guest OS is covered by you.

## Network connectivity
{: #network-connectivity}

Virtual private network (VPN) connectivity to the {{site.data.keyword.cloud_notm}} Virtual Cloud Network is granted automatically when your {{site.data.keyword.cloud_notm}} account is set up. By default, your server has a public and private IP address. If you want your server to be private, you can either turn off the public interface after your server is provisioned or order your server as private. See [Getting started with Virtual Private Networking](/docs/iaas-vpn?topic=iaas-vpn-getting-started) for more information on {{site.data.keyword.cloud_notm}} VPN.

## Storage
{: #storage}

Local storage is provided with your {{site.data.keyword.baremetal_short}} and uses the {{site.data.keyword.cloud_notm}} private network virtual LAN (VLAN) to help provide enterprise-grade security while not obstructing administrator access. It is ideal for storage-intensive applications with high I/O needs, such as an OS, and database and application software. SAP NetWeaver server disk space depends on how your server is configured. Contact [{{site.data.keyword.cloud_notm}} Support](/docs/get-support?topic=get-support-getting-customer-support#getting-customer-support) for extension options if the local storage on your server is insufficient for your workload.

There are two types of storage for {{site.data.keyword.cloud_notm}}-block and file-from which to choose to perform backups and restores for SAP NetWeaver. Both types use input/output operations per second (IOPS), which are used to determine storage needs. IOPS are measured based on 16 KB block size with a 50/50 read/write mix. To achieve maximum IOPS on a volume, adequate network resources need to be in place. Other considerations include private network usage outside of storage and host side, and application-specific tunings (for example, IP stacks and queue depths). See [Getting started with Block Storage](/docs/BlockStorage?topic=BlockStorage-getting-started#getting-started) and [Getting started with File Storage](/docs/FileStorage?topic=FileStorage-getting-started#getting-started) for more information on storage tiers and performance.

## Deployment and management
{: #deployment-and-management}

{{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}} are deployed through the {{site.data.keyword.cloud_notm}} infrastructure customer portal or API after you create your {{site.data.keyword.cloud_notm}} customer account. The servers can be managed through the customer portal, API, or command line interface (CLI). More information can be found under [IBM Cloud Bare Metal Servers](https://www.ibm.com/cloud/bare-metal-servers){: external}.

## Support
{: #concept-support}

[{{site.data.keyword.cloud_notm}} Customer Support](/docs/get-support?topic=get-support-getting-customer-support#getting-customer-support) handles any support questions and issues that might arise using various outlets, including chat, phone, and case-based support. Customer support is offered at no cost to all {{site.data.keyword.cloud_notm}} customers and covers most cases that are placed each day. See [Getting Customer Support](/docs/get-support?topic=get-support-getting-customer-support#getting-customer-support) for more information.

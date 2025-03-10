---
title: "Security specification for Private Cloud VMmare under SecNumCloud qualification (EN)"
excerpt: "Discover features, security functions and best practices to use our Private Cloud VMware service under SecNumCloud qualification"
updated: 2024-05-21
---

## Objective

In addition to the responsibility model between OVHcloud and the customer for the Hosted Private Cloud powered by VMware service under the SecNumcloud qualification, made available in the Special Terms and Conditions of Service, the purpose of this guide is to present best practices and features that customer can adopt to use the service.

## 1 - Certifications

- ISO/IEC 27001
- ISO/IEC 27701
- ISO/IEC 27017
- ISO/IEC 27018
- HDS
- SecNumCloud
- SOC 1 type II
- SOC 2 type II
- CSA type II
- C5 type II
- CISPE

## 2 - Best practices to deploy on the service

### 2.1 - Recommendations once the service is delivered

To access the vSphere interface under the SecNumCloud qualification, follow the steps on [the following link](/pages/hosted_private_cloud/hosted_private_cloud_powered_by_vmware/snc_getting_started) to authorize IP address connections to the vCenter, user access and authentication in MFA, as well as the network filtering and encryption features to secure the service.
You will also need to harden your operating system after you have created your virtual machines.

Other guides are available in the documentation set dedicated to the service on [this link](/pages/hosted_private_cloud/hosted_private_cloud_powered_by_vmware/snc_getting_started) to assist the customer in getting started with and using the service.

### 2.2 - Vulnerability Scans

You are authorized to perform vulnerability scans on the service you have subscribed to. OVHcloud doesn't have to be previously informed.
Security measures deployed by OVHcloud (especially network protection) aren't disabled, because such an audit's purpose is to demonstrate a clear vision of the security level of the customer's infrastructure.

You are not authorized to use your service to scan other infrastructures.

## 3 - SLA

| **Component** | **SLA** | **Calculation method** | **Compensation** |
| --- | --- | --- | --- |
| All components of the service | The monthly availability rate is 99.95% for the entire service | The total number of minutes in the month in question minus the number of minutes of unavailability over the month in question, where the total is divided by the total number of minutes in the month in question. To calculate the service credits, periods of unavailability are calculated when the incident is reported to OVHcloud by opening a ticket via the interface or via a call to support, until the outage is resolved and confirmation of the resolution is communicated by OVHcloud | 1. If monthly availability rate is < 99.95%, credit of 10% of the price on impacted service <br>2. If monthly availability rate is < 99%, credit of 30% of the price on the impacted service  |

The SLA for options such as Veeam Managed Backups may be different, please refer to the option's Special Terms and Conditions for more details. 

## 4 - Backups

### 4.1 - Technical backups

Technical backups are backups made by OVHcloud to maintain the Service Level Agreement. These backups cannot be activated at the customer's request.

### 4.2 - Sauvegardes métier

List of backup features and options adapted to the service.

| **Option name** | **Granularity** | **RPO** | **RTO** | **Documentation and tutorials**| **Jobs encryption**|
| --- | --- | --- | --- | --- | --- |
| Veeam Managed Backup(Advanced) | the VM | Depends on the date of the last backup and how long it takes to resolve the case | Depends on the size of the VM backed up | [Activate and use Veeam Managed Backup](/pages/hosted_private_cloud/hosted_private_cloud_powered_by_vmware/veeam_backup_as_a_service) | yes |
|Veeam Managed Backup(Premium) | the VM | Depends on the date of the last backup and how long it takes to resolve the case | depends on the size of the VM backed up | [Activate and use Veeam Managed Backup](/pages/hosted_private_cloud/hosted_private_cloud_powered_by_vmware/veeam_backup_as_a_service) | yes |

## 5 - Logs

Customers with a SecNumcloud-qualified Hosted Private Cloud infrastructure have the option of retrieving logs from the OVHcloud Control Panel, as well as the events recorded on the service they are operating.

> [!primary]
> Follow this guide [First steps with OVHcloud API](/pages/manage_and_operate/api/first-steps) to understand how to use   OVHcloud APIv6.

| **Source** | **Content** | **Links** |
| --- | --- | --- |
| Control Panel | Logs of interactions made by admin, technical or billing contacts in the Control Panel and services they have access to, using API calls. |- <https://api.ovh.com/console/#/me> (see `/me/api/logs`)<br>- [List of API calls done with your account](https://api.ovh.com/console/#/me/api/logs/self~GET)<br>- [List of API calls done on services you have access to](https://api.ovh.com/console/#/me/api/logs/services~GET)<br>- [Get your audit logs](https://api.ovh.com/console/#/me/logs/audit~GET) |
| Service | Tasks and events history on the vCenter carried out by a customer on their infrastructure. |vSphere Client, "Tasks and events" sheet or via an API call for certain tasks: <br> [Tasks associated with this User](https://api.ovh.com/console/#/dedicatedCloud/%7BserviceName%7D/user/%7BuserId%7D/task~GET) |
| Service | Logs of "support user" which correspond to tasks, performed by an OVHcloud user created on the fly, in the customer's infrastructure for support and incident management. | vCenter History: vSphere Client, "Tasks and events" sheet|

## 6 - API

| **Name** | **Capacity** | **Documentation** |
| --- | --- | --- |
| Control Panel and service | Manage customer accounts and services on which each account has access rights. | [API calls for Private Cloud](https://api.ovh.com/console/#/dedicatedCloud) |

## 7 - Users accounts

### 7.1 - Control Plane

Using your customer account on the OVHcloud Control Panel, you are able to manage your service using [three different contacts](/pages/account_and_service_management/account_information/managing_contacts).<br>
OVHcloud uses another account with an internal NIC to refer a customer having subscribed to several services.

To enforce security access to your account on the Control Panel, we recommend activating a [two-factor authentication mechanism](/pages/account_and_service_management/account_information/secure-ovhcloud-account-with-2fa).

You can manage user access to the vSphere interface with IP filtering and two-factor authentication by following the first steps in [this guide](/pages/hosted_private_cloud/hosted_private_cloud_powered_by_vmware/snc_getting_started).

With the administrator account, you are able to establish your own access policy to the vCenter, to create users and assign them different access rights to manage the resources, to access to the vSphere interface and management of the private and public network part. Guide and configuration details are available on [this link](/pages/hosted_private_cloud/hosted_private_cloud_powered_by_vmware/manager_ovh_private_cloud).

### 7.2 - Data Plane

You are autonomous to create user accounts on your Operating System, once you have the admin rights on your server. 

## 8 - Antivirus

Anti-virus protection, with weekly scans, is deployed on various components of the infrastructure managed by OVHcloud, such as the SSL Gateway, the Private Gateway and the Master zone, etc.

There is no protection in place for the VMs deployed by the customer, so it is the customer’s responsibility to install their own antivirus software and monitor it.

## 9 - Features and options available at service delivery

### 9.1 - VM images

OVHcloud offers customers VM templates in OVF format. These VM templates have a minimum level of hardening. The level of hardening for Windows OS and Linux distribution refers to the nominal installation of the editor. For an advanced hardening level, we recommend that you refer to the guidelines published by each editor.

When you deploy a VM, you can also import your own ISO image.

### 9.2 - Filtering functions, encryption and other security options

### 9.2.1 SSL Gateway

IP addresses of a Private Cloud service to access the VMware admin interface are public by default.

The SSL Gateway is a gateway that allows a customer to activate filtering functions to allow their own users to connect to their infrastructure through Internet network.

It also offers a Firewall/NAT service that you can configure using 'iptable', a certificate to secure the connection, a ProxyPass, monitoring, an SFTP server and an antivirus script with daily/updated scan. 


### 9.2.2 Private Gateway

The Private Gateway is an option available on a Private Cloud service and activated by default on a SecNumCloud qualified infrastructure. It allows the customer to manage access to their infrastructure via a private IP (vSphere interface, vScope, etc.). 

Once deployed, the Private Gateway acts as a proxy to access the infrastructure from the vRack network. All the rules established in SSL Gateway (iptable) will be copied to the Private Gateway for filtering. Access via public IPs will be disabled and the Private Cloud domain will only be accessible via this Gateway.   

The procedure for enabling Private Gateway is available here: [Activate the Private Gateway](/pages/hosted_private_cloud/hosted_private_cloud_powered_by_vmware/private_gateway).

For SecNumCloud-qualified infrastructure, you will need to follow Step 4, available here: [Getting started with vSphere SecNumCloud](/pages/hosted_private_cloud/hosted_private_cloud_powered_by_vmware/snc_getting_started).

### 9.2.3 NSX

Several network filtering features such as micro segmentation, distributed firewall, load balancing, etc. are available via VMware's NSX-based SDN solution.

The guide to getting started with the NSX solution is available on [this link](/pages/hosted_private_cloud/hosted_private_cloud_powered_by_vmware/nsx-01-first-steps). It is accompanied by other tutorials in the documentation space to facilitate the use of other features.

### 9.2.4 SecNumCloud Connectivity: SPN and VPN

An optional connectivity service is available on SecNumCloud qualified infrastructure. This service option includes:

- A Secure Private Network  (SNC Secured Private Network or SPN);
- A secure interconnection between remote SPNs (SNC SPN Inter-DC);
- An IPsec VPN gateway (SNC VPN Gateway).

An overview of these options is available on [this link](/products/hosted-private-cloud-hosted-private-cloud-powered-by-vmware-networking-secnumcloud-connectivity).

### 9.2.5 Data encryption

On a SecNumcloud or non-SecNumcloud qualified infrastructure, you can apply encryption at rest using the vNKP brick available on the service to encrypt VMs or at the datastore level of a vSAN Cluster.

The same operation can be carried out if the customer chooses to use a KMS external to the OVHcloud solution.

Instructions for use are available on [this link](/pages/hosted_private_cloud/hosted_private_cloud_powered_by_vmware/vm_encrypt-vnkp).

### 9.2.6 Advanced security with HDS

You can benefit from an advanced security pack by enabling HDS options on your infrastructure.

The pack includes several features such as: [token validator](/pages/hosted_private_cloud/hosted_private_cloud_powered_by_vmware/interface-secure), access via 2FA, session timeout, fail2ban, hids, force TLS v1.2 protocol, etc.

## 10 - Reversibility

To ensure data portability and reversibility on the service, OVHcloud allows you to import and export your data (virtual machines and vCenter configuration files) autonomously in a VMDK file format or any other format supported by the VMware hypervisor. You can also use the APIs provided to facilitate these operations.

OVHcloud’s portability principles are described in its own [reversibility policy](/pages/account_and_service_management/reversibility/00-global-reversibility-policy) and those specific to the Hosted Private Cloud by VMware service qualified SecNumCloud are set out [specific policy](/pages/account_and_service_management/reversibility/05-snc-vmware-reversibility-policy).

### 10.1 - Erasure of customer data 

Following the customer’s decommission of the service and prior to the removal of the hard drive from the rack, an erasing robot applies a secure data erasure procedure based on the NIST SP 800-88 r1 level ‘Purge’. In case of technical constraints or limitations on certain ranges of hard drives and when the level 'Purge' cannot be applied, the erase at the level 'Clear' will run.

On an infrastructure qualified as SecNumCloud, the 'Destroy' level is applied after the disk has been extracted from the array.

### 10.2 - Erasure of technical data

Following the customer’s resignation from the service, OVHcloud releases the resources allocated to him and deletes the configurations made during service delivery

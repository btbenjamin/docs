---
title: "Connettere un'immagine ISO a una VM (EN)"
excerpt: "How do you connect an ISO image to a virtual machine?"
updated: 2024-11-05
---

> [!success]
> You can refer to the guide [Upload an ISO to a datastore](/pages/hosted_private_cloud/hosted_private_cloud_powered_by_vmware/vmware_datastore_upload) for more information on uploading elements (ISO, files, etc.) to your VMware on OVHcloud environment.

## Objective

You can set up an ISO library in your infrastructure to be used for OS and software deployment.

**This guide will run you through the process of connecting an ISO image to a VM.**

## Requirements

- Being an administrative contact of your [Hosted Private Cloud infrastructure](/links/hosted-private-cloud/vmware) to receive login credentials
- A user account with access to vSphere (created in the [OVHcloud Control Panel](/links/manager))

## Instructions

### Library Creation

In the vSphere interface menu, go to the `Storage`{.action} section.<br>
Choose the Datastore you will be building the library in (prefer Shared Storage over Local to avoid file access issues).<br>
In the `Files`{.action} tab, Click on `New Folder`{.action}.

![FOLDER](images/en01newfolder.png){.thumbnail}

After naming your folder (ISOs in our study case), select it and click `Upload Files`{.action}.

![UPLOAD](images/en02upload.png){.thumbnail}

Browse to the ISO file(s) you wish to upload and click `Open`{.action}.

![BROWSE](images/en03browse.png){.thumbnail}

Your library is set. You can add more ISO images as you need and as storage space allows.

![LIBRARY](images/en04library.png){.thumbnail}

### Connect Image to VM

In the vSphere interface menu, go to the `Hosts & Clusters`{.action} section.<br>
Right click the VM you need the ISO image attached to and click on `Edit Settings`{.action}.<br>

![EDIT](images/en05edit.png){.thumbnail}

Change the CD/DVD drive setting to Datastore ISO File.

![ISO](images/en06dataiso.png){.thumbnail}

In the browsing window that pops up, navigate to the library previously created and select the image you wish to use.

Click on `OK`{.action}.

![SELECT](images/en07choose.png){.thumbnail}

Back in the "Edit Settings" menu, make sure the "Connect" box is checked and click `OK`{.action}.

![CONNECT](images/en08connect.png){.thumbnail}

The ISO image is now connected to your VM and can be accessed as if it were an attached physical media.

## Go further

To go further with uploads within your Hosted Private Cloud - VMware on OVHcloud environment, please refer to the guide [Uploading an ISO into a datastore](/pages/hosted_private_cloud/hosted_private_cloud_powered_by_vmware/vmware_datastore_upload).

You can use your vCenter on OVHcloud secure HTML web client, as well as `govc` (see the procedure in the guide).

Join our [community of users](/links/community).

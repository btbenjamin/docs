---
title: Public Cloud Databases - Getting started with APIs
excerpt: Find out how to order and manage your Public Cloud managed database service using the OVHcloud API
updated: 2024-02-29
---

## Objective

Public Cloud managed databases allow you to focus on building and deploying cloud applications while OVHcloud takes care of the database infrastructure and maintenance.

**This guide explains how to order a MongoDB instance of a Public Cloud managed database service using the OVHcloud API.**

## Requirements

- access to the [OVHcloud API](https://api.ovh.com/){.external} (create your credentials by consulting [this guide](/pages/manage_and_operate/api/first-steps))
- a [Public Cloud project](https://www.ovhcloud.com/asia/public-cloud/) in your OVHcloud account

## Instructions

### Step 1: Gather the set of required parameters

In order to create a database service, you will need to specify at minimum:

- an _engine_, and its _version_ (e.g. "MongoDB "6.0")
- the _plan_ (e.g. "business")
- the _nodes_ of the cluster (e.g. "3 nodes with 4 cores, 15 GiB memory, 100 GiB disk")

#### List the capabilities

The _capabilities_ endpoint lists the allowed values for the engine, plan, and flavor the service knows about.

> [!api]
> @api {v1} /cloud GET /cloud/project/{serviceName}/database/capabilities

The call returns an object listing allowed values for:

- the various engines, with the various versions for each engine
- the plans
- and the flavors

#### Get the availability

The _availability_ endpoint lists what combination of parameters the service allows. For example, a MongoDB `Essential` plan currently allows clusters with a single node, whereas `Business` services allow clusters of 3 to 8 nodes. You should decide what set of parameters among that list best fit your needs.

> [!api]
> @api {v1} /cloud GET /cloud/project/{serviceName}/database/availability

The call returns an array listing the available set of parameters. Each entry in this array lists (among other data): an _engine_, a _version_, a _plan_, a _flavor_, a _region_, if it supports _public_ or _private networking_, a _minimum number of nodes_ and a _maximum number of nodes_.

### Step 2: Create a MongoDB database service

> [!warning]
> By creating a cluster, you will be billed accordingly.

Use this endpoint to create a new database cluster:

> [!api]
> @api {v1} /cloud POST /cloud/project/{serviceName}/database/mongodb

- **description**: A human-readable description for the service you wish to create
- **plan**: the desired plan for the service
- **version**: the MongoDB version you want to use
- **nodesPattern**: specify the _flavor_ and _region_, and the number of nodes you want to use
- **nodeslist**: Leave this parameter undefined. It is another way to specify the list of nodes your cluster uses. As of today, multi-region and flavor-heterogeneous clusters are not supported. Hence it is easier to use **nodesPattern** to specify a number of same-region, same-flavor nodes.
- **ipRestrictions**: The IP addresses blocks allowed to connect to your cluster.

> [!primary]
> For security reasons, the default network configuration does not allow any incoming connections. You must authorize a suitable IP address to successfully access your database.

If you want to use public networking, you're all set. If you want to use private networking, you'll also want to specify:

- **networkId**: The ID of the vRack you want to use
- **subnetId**: The ID of the vRack subnet you want your cluster to be attached to

The call returns an object describing the cluster you asked for. Initially, its **status** property will be `CREATING`. Take note of the **id** property of the newly-created cluster for the next step.

### Step 3: Wait for your database service to be ready

The cluster will take a few minutes to become fully usable. You can check its status using:

> [!api]
> @api {v1} /cloud GET /cloud/project/{serviceName}/database/mongodb/{clusterId}

The call returns an object describing the cluster. Its **status** property will transition to `READY` when the cluster becomes available.

### Step 4: Reset the primary user password

At this point you don't know your cluster primary user's password. List your cluster's users with:

> [!api]
> @api {v1} /cloud GET /cloud/project/{serviceName}/database/mongodb/{clusterId}/user

Note the id of your admin user. Reset its password with:

> [!api]
> @api {v1} /cloud POST /cloud/project/{serviceName}/database/mongodb/{clusterId}/user/{userId}/credentials/reset

Note the new password of the user to later be able to connect to the cluster.

> [!warning]
> That password won't ever be available later on: OVHcloud never stores users' passwords.

### Step 5: Start using the cluster

You’ll find the cluster connection information in your Control Panel; you can now start using the cluster!

## Go further

[MongoDB capabilities](/pages/public_cloud/public_cloud_databases/mongodb_01_concept_capabilities)

[Managing a MongoDB service from the OVHcloud Control Panel](/pages/public_cloud/public_cloud_databases/mongodb_02_manage_control_panel)

[Configuring vRack for Public Cloud](/pages/public_cloud/public_cloud_network_services/getting-started-07-creating-vrack)

Visit our dedicated Discord channel: <https://discord.gg/ovhcloud>. Ask questions, provide feedback and interact directly with the team that builds our databases services.

If you need training or technical assistance to implement our solutions, contact your sales representative or click on [this link](https://www.ovhcloud.com/asia/professional-services/) to get a quote and ask our Professional Services experts for a custom analysis of your project.

Join our community of users on <https://community.ovh.com/en/>.

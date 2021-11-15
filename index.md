---
title: Quick Guide for Teradici CAS and Nvidia Omniverse
description: Steps to get started with Teradici CAS and Nvidia Omniverse solution for remote collaboration
author: chad-m-smith
tags: CAS,PCoIP, Omniverse 
date_published: 2021-11-11
---

Chad Smith | Technical Alliance Architect at Teradici | HP

<p style="background-color:#CAFACA;"><i>Contributed by Teradici employees.</i></p>

This script is designed to allow Teradici end users to power on their EC2 instances remotely without having to access the EC2 dashboard. It will also find the public or elastic IP of the instances and pass the connection info to a PCoIP connection string automatically. While larger Teradici deployments will benefit from [Cloud Access Manager (CASM)](https://www.teradici.com/web-help/cas_manager_as_a_service/) when multiple instances reside in the same region. It is cost prohibited to run CASM connection gateways (CAC) when only a handful of user’s instances per region are needed and/or customer are interested in leveraging AWS local zones where the cost of perpetually running a CAC is cost prohibited.

**AWS EC2 PCoIP Quick connect script workflow, components and dependencies.**

   ![image](https://github.com/ChadSmithTeradici/AWS_EC2_PCoIP_QuickConnect_Script/blob/main/images/AWS_EC2_PCoIP_QuickConnect.jpg)

## Objectives

+ Create EC2 instances in AWS.
+ Create an IAM role/policy to lock down access to instances
+ Apply Policy to user and programmatic access to resources 
+ Download and configure AWS CLI 
+ Install PCoIP Client software
+ Create script and set permission on client.


## Costs

This tutorial uses billable components of AWS Cloud and assumes Teradici subscription, including the following:
+   [AWS EC2 Instance](https://aws.amazon.com/pm/ec2/), including vCPUs, memory, disk, and GPUs
+   [Internet egress and transfer costs](https://aws.amazon.com/blogs/architecture/overview-of-data-transfer-costs-for-common-architectures/), for PCoIP and other applications communications.

Use the [AWS pricing calculator](https://calculator.aws/#/) to generate a cost estimate based on your projected usage.


---
title: Quick Guide for Teradici CAS and Nvidia Omniverse
description: Steps to get started with Teradici CAS and Nvidia Omniverse solution for remote collaboration
author: chad-m-smith
tags: CAS,PCoIP, Omniverse 
date_published: 2021-11-15
---

Chad Smith | Technical Alliance Architect at Teradici | HP

<p style="background-color:#CAFACA;"><i>Contributed by Teradici employees.</i></p>

This deployment guide is designed to get users up and running quickly with the Teradici and Omniverse bundle. For reference, Teradici CAS provides pixel and color accurate representation of host systems remotely across great distances, while Omniverse allows for in application collaboration between participates.  Our solutions work in conjunction to provide remote users the ability to collaborate and conduct real-time photorealistic simulation using their native applications regardless of the distance between them. 

There are **three deployment scenarios** for workstations with Teradici CAS and Omniverse software. 
+ **1st scenario:** Is when the device will be used remotely to log into centralized infrastructure which is hosting applications, CAS client is installed on the workstation. 
+ **2nd scenario:** Is when the workstation/laptop will be used as a host for applications and a secondary device, such as a CAS, thin or zero client will make a connect to the workstation remotely. In this situation CAS agent is installed on the workstation. 
+ **3rd scenario:** Is when a workstation hosts applications but need access to remote applications as well, the workstation can act as both a host and client depending on the situation, this is when both the CAS agent and client is installed on the workstation.

As it pertains to Omniverse, it generally is installed on the host system(s) that themselves particiapte in a local area networks (LANs) for optimal real-time in application collaboration. The Necleus server role 

![image](https://github.com/ChadSmithTeradici/Teradici_CAS_Omniverse_deployment_guide/blob/main/images/QS-CASandOmniverseDiagram.jpg)

## Objectives

+ Understanding network topology ports opened for Application access
+ Install Teradici CAS software.
+ Install Nvidia Omniverse
+ Creating your first project



## Installing Teradici CAS

1. Obtain registration key

1. Register on Teradici protal to obtain software

1. Download softward depending on OS host requirements

1. Install software (dependencies on GPU driver being installed)

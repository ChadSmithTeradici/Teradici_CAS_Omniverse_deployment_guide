---
title: Quick Guide for Teradici CAS and Nvidia Omniverse
description: Steps to get started with Teradici CAS and Nvidia Omniverse solution for remote collaboration
author: chad-m-smith
tags: CAS,PCoIP, Omniverse 
date_published: 2021-11-15
---

Chad Smith | Technical Alliance Architect at Teradici | HP

<p style="background-color:#CAFACA;"><i>Contributed by Teradici employees.</i></p>

This deployment guide is designed to get user quickly up and running with Teradici and Omniverse bundle. 

There are three deployment scenarios for workstations/laptops for Teradici CAS and Omniverse software. The first scenario is when the device will be used remotely to log into centralized infrastructure which is hosting applications, CAS client is installed on the workstation. The second scenario is when the workstation/laptop will be used as a host with applications installed and a secondary device, such as a CAS, thin or zero client will make a connect to the workstation. In this situation CAS agent is installed on the workstation The third scenario is when a workstation hosts applications but need access to remote applications that is when the CAS agent and client is installed on the workstation.

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

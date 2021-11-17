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
+ **Scenario 1:** Is when the device will be used remotely to log into centralized infrastructure which is hosting applications, CAS client is installed on the workstation. 
+ **Scenario 2:** Is when the workstation/laptop will be used as a host for applications and a secondary device, such as a CAS, thin or zero client will make a connect to the workstation remotely. In this situation CAS agent is installed on the workstation. 
+ **Scenario 3:** Is when a workstation hosts applications but need access to remote applications as well, the workstation can act as both a host and client depending on the situation, this is when both the CAS agent and client is installed on the workstation.

As it pertains to **Omniverse** in these deployment scenarios, it generally is installed on the host system(s) that are usually on a local area networks (LANs) with the other participating workstations for optimal real-time collaboration. Remote contributers will connect into a workstation that has all applications, including Omniverse installed. Files can either be kept local or centralized on NAS (network attached storage) with a Necleus server acting a syning mechanism between participants. The Necleus server does have build-in file synch and share service, but doesn't allow for real-time collaboration between participates when working remotly, which diminishes the value of Omniverse. The illustration below shows each of the deployment senerios that will be discussed:

![image](https://github.com/ChadSmithTeradici/Teradici_CAS_Omniverse_deployment_guide/blob/main/images/QS-CASandOmniverseDiagram.jpg)

## Objectives

+ Understanding network topology ports opened for Application access
+ Install Teradici CAS software.
+ Install Nvidia Omniverse
+ Creating your first project

## Opening port for communications

Omniverse communications happens between workstations that have Neculeus Workstation applaiction, Neculeus Server / Database and any file services holding the USD files. These services typically are installed on the 

![image](https://github.com/ChadSmithTeradici/Teradici_CAS_Omniverse_deployment_guide/blob/main/images/Firewall%20rules.jpg)

## Scenerio 1: Installing Teradici CAS client Client and connect to a Host
In this section, you will establish a connection to your instance using PCoIP. You will need to install a PCoIP client on your client system that will be used to initiate the session to the EC2 Mac Instance in AWS. Depending on your network topology, use will either connect to the local IP (or) ephemeral/elastic Public IP (or) Fully Qualified Domain Names (FQDN)

1. [Download the client installer](https://docs.teradici.com/find/product/software-and-mobile-clients) based on your client OS. You don't need a login credentials to download client software and can have as many copys of various client OS as you need.

1. Install the PCoIP client software per the OSs Administration Guides installation instructions.

1. Locate the **IP address** or **FQDN** of the AWS EC2 Mac instance via the [EC2 Dashboard](https://console.aws.amazon.com/ec2)

1. Identify the Mac instance within the list of **Running Instances** in the EC2 Dashboard, check the **box** near the instance name, if it was named.

1. Under the **Details** tab you will see **Public IPv4 Address** (or) **Private IPv4 Address** (or) **Private IPv4 DNS** (or) **Public IPv4 DNS**

1. From the client system, start your PCoIP client per OS. Typically the PCoIP client will have a icon:

    ![image](https://github.com/ChadSmithTeradici/TeradiciPCoIPonMACinAWS/blob/main/images/PCoIP_icon.jpg)

1. When the PCoIP client starts, it will ask for a **Host Address or Code**. Enter in your **IP address or FQDN** previously identified in previous section. (optionally) enter a name to **Connection Name** field then **SAVE**, if you want to save connection.

    ![image](https://github.com/ChadSmithTeradici/TeradiciPCoIPonMACinAWS/blob/main/images/PCoIP-Client.jpg)
    
1. Next, you will get a Cannot verify your connection to IP warning. This error is becuase a 3rd party trusted certificate has not been install on the host. You can select the **Connect Insecurely** option.
    
    ![image](https://github.com/ChadSmithTeradici/TeradiciPCoIPonMACinAWS/blob/main/images/PCoIP-Trusted.jpg)
    
1. Finally, enter in the macOS login credentials(**ec2-user**, if not changed)that you used previously in your VNC session to log into the instance.

    ![image](https://github.com/ChadSmithTeradici/TeradiciPCoIPonMACinAWS/blob/main/images/PCoIP-Auth.jpg)




## Installing Teradici CAS agent on host

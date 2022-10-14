---
title: "API resources"
date: 2022-06-08T16:05:49+01:00
draft: false
weight: 1
description: General info about API resources running through Azure Cloud Provider
---

## General Architecture
There is a Windows VM which has been deployed which acts as a resource to run the POS API. On this VM we are able to start the POS test server  
which the client uses to send and receive data from.

### HungerRush Handheld Infrastructure

This [repository](https://github.com/IIIMPACT/hungerrush-handheld-infrastructure) represents the IaC for the HungerRush Handheld project and is built and maintained in Terraform.
You can also login into Azure portal using the **iciuser@devrevention.onmicrosoft.com** (password can be obtained from an active dev) to view the deployed resources.

### Connecting to the Windows VW
In order to restart the POS test server the following 2 application are used:

- **Teamviewer** -> connect file transfer with id **953 138 928** (Teamviewer session & Windows VM passwords can be obtained from any of the active developers)
- **Microsoft Remote Desktop** (requires VPN, needs fixing since we currently don't have VPN access anymore)

### Solutions Overview

There are 12 solution in RevCloudPOS of which some are more relevant than others: 
- **DataService** defines the main data services that we use frequently on the POS client 
- **RevCloudPos** is a shared project for POS services
- **RevCloudPos.Android** is the sample Android Project
- **RevCloudPos.IOS** is the sample IOS Project
- **RevCloudPos.UWP** is the sample Windows App
- Multiple **HurgerRushPOS** type solutions for different platforms are older and we don't use them actively

### Building & Integrating Solutions

In order to build & integrate solutions you need to:
- Select property on the e.g. DataService
- Select Class Library as type
- Select >  .NET 2.0 version in order for Xamarin to be compatible with the libraries
- Go to the output in DataService/bin/Debug(or Release)/netstandart2.0 to find the DataService.dll
- This DataService.dll can then be integrated into the Hand Held client 


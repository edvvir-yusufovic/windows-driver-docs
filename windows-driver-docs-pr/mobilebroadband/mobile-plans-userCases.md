---
title: Mobile Plans Use Cases
description: This topic describes the basic user cases that Mobile Operators could implement.
ms.assetid: 24050B13-4A1A-466F-974B-40B34EDB16DC
keywords:
- Windows Mobile Plans User cases, Mobile Plans implementation mobile operators
ms.date: 03/15/2018
ms.localizationpriority: medium
---

# Mobile Plans Use Cases

## Overview

This topic provides insights about most common use cases that mobile operators are planning to enable, this is not an exhaustive list of supported cases. It is probable that your specific user case could be achivied via a combination of solutions. Please reach your Microsoft contact to discuss further your scenario.

## Install an eSIM profile in a Windows device

This section describes what a mobile operator should implement to activate, download and install an eSIM profile in a Windows device. Depending on which are the particular conditions of your network backend and how long the activation process will take you could choose to implement more than one way to return control to Mobile Plans app. 

Please follow these steps:

1. Implement the Mobile Operator web portal.
2. Implement the adequate control back to Mobile Plans
   1. **Inline profile Delivery**, implement this callback if the eSIM profile is immediatelly available in the SMDP+ server and the device will be able to attach to the cellular network immediatelly.
   2. **Asynchronous Connectivity**, implement this callback if the eSIM profile is immediatelly available in the SMDP+ server but the device will need to wait some time before attach to the cellular network.
   3. **Asynchronous Profile Donwload**, implement this callback if the eSIM profile will be available in your SMDP+ server after a period of time and the device wiil be able to attahc to the cellular network immediatelly.
3. Handling eSIM download errors

4. Define your user experience once the device is active.

## Add balance to our current subscription

This section describes which work is needed to add balance to your current subscription, this is useful if you are selling prepaid plans or if you sell data packages once a postpaid subscription runs out of Internet data.

1. Support the Walled Garden
2. Implement the Get Balance API, this will ensure that you are able to control the behavior of network flyout depending in the status of the subscription
3. Implement the Mobile Operator web portal (eSIM)
4. Implement the adding balance control back to Mobile Plans


### Experience after instalation

Unlimited data with out GetBalance Implementation

Mobile operator has to decide which will be the user experience after a the esIM profile is installed in the device. The network flyout is the place where the user will interact after a profile is downloaded

<<Add an image of netowork flyout>>





if you are planning to show balance date information in the network flyout, please ensure that you implement Get Balance API (link to getbalance)






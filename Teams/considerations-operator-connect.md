---
title: Considerations for Operator Connect
author: CarolynRowe
ms.author: crowe
manager: serdars
ms.reviewer: roykuntz
ms.date: 04/14/2023
ms.topic: article
ms.assetid: 589bf5f5-490a-4215-8588-99bab7d33e31
ms.tgt.pltfrm: cloud
ms.service: msteams
search.appverid: MET150
ms.collection:
  - M365-voice
  - m365initiative-voice
  - highpri
  - Tier1
audience: Admin
appliesto:
  - Microsoft Teams
ms.localizationpriority: medium
f1.keywords:
- CSH
ms.custom:
  - ms.teamsadmincenter.locations.emergencyaddresses.overview
  - ms.lync.lac.AddressAndLocation
  - Calling Plans
  - Direct Routing
description: "Learn about emergency calling, including information about emergency addresses, emergency call routing, and dynamic emergency calling."
---

# Considerations for Operator Connect

This article describes considerations for emergency calling for Operator Connect users. Before reading the rest of this article, make sure you've reviewed critical emergency calling concepts and definitions in [Plan and manage emergency calling](what-are-emergency-locations-addresses-and-call-routing.md).

To find out whether Operator Connect is the right solution for your business, see [PSTN connectivity options](pstn-connectivity.md) and [Plan for Operator Connect](operator-connect-plan.md).

## Emergency call enablement for Operator Connect

Each Operator Connect user is automatically enabled for emergency calling. Emergency calls are routed automatically to the Operator Connect carrier for a given number.

The ability for a tenant admin to set the registered address for an Operator Connect user will depend upon the capabilities assigned to the number when the carrier uploads them into a customer's inventory. Based upon this setting, the tenant administrator may or may not be required&mdash;or able&mdash;to set, modify, or delete the emergency location of a user.

## Dynamic emergency calling for Operator Connect

Dynamic emergency calling for Operator Connect provides the capability to configure and route emergency calls based on the current location of the Teams client. The ability to do automatic routing to the appropriate Public Safety Answering Point (PSAP) or to notify security desk personnel varies depending on the country of usage of the Teams user.

Dynamic location for routing emergency calls is supported in the United States as follows.

- If a Teams client for a United States user dynamically acquires an emergency address within the United States, that address is used for emergency routing instead of the registered address, and the call will be automatically routed to the PSAP in the serving area of the address.

- If a Teams client for a United States user doesn't dynamically acquire an emergency address within the United States, then the registered emergency address is used to help screen and route the call. However, the call will be screened to determine if an updated address is required before connecting the caller to the appropriate PSAP.

Dynamic location for routing emergency calls is supported in Canada the same as in the United States with the following exceptions: all emergency calls will be screened nationally before transferred to the PSAP.

For more information, see [Plan and configure dynamic emergency calling](configure-dynamic-emergency-calling.md).

## Emergency call routing for Operator Connect

When a Teams Operator Connect user dials an emergency number, how the call is routed to the PSAP depends on the following:

- Whether the emergency address is dynamically determined by the Teams client

- Whether the emergency address is the registered address associated with the user's phone number

- The emergency calling network of that country

- In the United States and Canada, dynamic routing is part of the carrier's service. You don't need to procure this service from another service provider.

- If a Teams client is located at a tenant-defined dynamic emergency location:
  - In the United States, emergency calls from that client are automatically routed to the PSAP serving that geographic location.
  - In Canada, all emergency calls will be screened by a national call center before transferring the call to the PSAP serving that geographic location.

- If a Teams client is not located at a tenant-defined dynamic emergency location, emergency calls from that client are screened by a national call center to determine the location of the caller before transferring the call to the PSAP serving that geographic location.

- If an emergency caller is unable to update their emergency location to the screening center, the call will be transferred to the PSAP serving the caller's registered address.

## Related topics

- [Plan and manage emergency calling](what-are-emergency-locations-addresses-and-call-routing.md)
- [Manage emergency calling policies](manage-emergency-calling-policies.md)
- [Manage emergency call routing policies](manage-emergency-call-routing-policies.md)
- [Plan and configure dynamic emergency calling](configure-dynamic-emergency-calling.md)
- [Plan for Operator Connect](operator-connect-plan.md)

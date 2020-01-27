---
nav_title: "Push Registration"
page_order: 3
page_type: reference
description: "This reference article covers the concept of Push Registration."

channel:
  - push
tool:
  - Docs
  - Dashboard
  - Campaigns
---

# Push Registration

> This reference article covers the process through which users get registered for push. 

A huge aspect of Push Registration involves Push Tokens. A Push Token is the identifier that senders use to target specific devices with a push notification. If a device does not have a push token, there is no way to send push to it. 

Push Tokens are generated by Push Service Providers the Firebase Cloud Messaging Service (FCMs) or Apple Push Notification Service (APNs) respectively. Each device has one, unique token that is used for messaging. Tokens can expire or be updated.

| Get a Push Token | Send a Push Token |
| ---------------- | ----------------- |
| Applications must register with a push provider in order to get a push token for a device. | Developers can then target the device using the push token generated by FCM/APNs.|

![Picture][push-process]


| Registration steps | Messaging steps |
| ------------------ | --------------- |
| 1. Customer (device) registers to push provider<br>2. Provider generates and delivers push token<br>3. Flush tokens in Braze |1. Braze sends push payload to provider<br>2. Provider delivers the push payload to device<br>3. SDK passes messaging stats to braze |

[push-process]: {% image_buster /assets/img/push_process.png %}
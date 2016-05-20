---
title: ios notification
date: 2016-05-20 01:08:34
tags:
---
 The essential purpose of both local and remote notifications is to enable an app to inform its users that it has something for them.

![ios notification](/resource/ios_notification/badged_app.png)

<!--more-->

* Local notifications are scheduled by an app and delivered on the same device.
* Remote notifications, also known as push notifications, are sent by your server to the Apple Push Notification service, which pushes the notification to devices.

## Local and Remote Notifications Appear the Same to Users
* Users can get notified in the following ways:

### An onscreen alert or banner
### A badge on the app’s icon
### A sound that accompanies an alert, banner, or badge

* When your app is frontmost, UIKit delivers local and remote notifications directly to your app delegate object without displaying any system UI. UIKit calls the application:didReceiveLocalNotification: method for incoming local notifications and the application:didReceiveRemoteNotification:fetchCompletionHandler: method for incoming remote notifications. Use the provided notification dictionary to update your app accordingly. Because your app is running, you can incorporate the notification data quietly or update your user interface and let the user know that new information is available.

## The remote notification 

* Each remote notification includes a payload. The payload contains information about how the system should alert the user as well as any custom data you provide. The maximum size allowed for a notification payload depends on which provider API you employ. When using the HTTP/2 provider API, maximum payload size is 4096 bytes. Using the legacy binary interface, maximum payload size is 2048 bytes. Apple Push Notification service (APNs) refuses any notification that exceeds the maximum size.

### Keys and values of the aps dictionary

| Key | Value type | Comment |
|:----:|:----:|
| alert | string or dictionary |If this property is included, the system displays a standard alert or a banner, based on the user’s setting.|
| badge | number |The number to display as the badge of the app icon.|
| sound | string |The name of a sound file in the app bundle or in the Library/Sounds folder of the app’s data container.|
| content-available | number |Provide this key with a value of 1 to indicate that new content is available. Including this key and value means that when your app is launched in the background or resumed, application:didReceiveRemoteNotification:fetchCompletionHandler: is called.|
| category | string |Provide this key with a string value that represents the identifier property of the UIMutableUserNotificationCategory object you created to define custom actions. To learn more about using custom actions.|

### Child properties of the alert property


| Key | Value type | Comment |
|:----:|:----:|
| title | string |A short string describing the purpose of the notification.|
| body | string |The text of the alert message.|
| title-loc-key | string or null |The key to a title string in the Localizable.strings file for the current localization. The key string can be formatted with %@ and %n$@ specifiers to take the variables specified in the title-loc-args array.|
| title-loc-args | array of strings or null |Variable string values to appear in place of the format specifiers in title-loc-key.|
| action-loc-key | string or null |If a string is specified, the system displays an alert that includes the Close and View buttons. The string is used as a key to get a localized string in the current localization to use for the right button’s title instead of “View”.|
| loc-key | string |A key to an alert-message string in a Localizable.strings file for the current localization (which is set by the user’s language preference). The key string can be formatted with %@ and %n$@ specifiers to take the variables specified in the loc-args array. |
| loc-args | array of strings |Variable string values to appear in place of the format specifiers in loc-key. |
| launch-image | string |The filename of an image file in the app bundle, with or without the filename extension. |

```
{
   "aps" : {
      "category" : "NEW_MESSAGE_CATEGORY"
      "alert" : {
         "body" : "Acme message received from Johnny Appleseed",
         "action-loc-key" : "VIEW"
      },
      "badge" : 3,
      "sound" : “chime.aiff"
   },
   "acme-account" : "jane.appleseed@apple.com",
   "acme-message" : "message123456"
}
```

[REFERENCE](https://developer.apple.com/library/ios/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/Chapters/TheNotificationPayload.html#//apple_ref/doc/uid/TP40008194-CH107-SW4)

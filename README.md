NotificationListenerServiceDemo
===============================
Android NotificationListenerService Demo.base on ([NotificationListenerService-Example][1])

## Introduction
NotificationListenerService allows an third-party application to receive notification information. 
More information please contact ([developer.android.com][2])

## ScreenShot

![Image][3]
![Image][4]

## Useful Methods
1. NotificationListenerService
	* onNotificationPosted(StatusBarNotification sbn)
	* onNotificationRemoved(StatusBarNotification sbn)
	* cancelAllNotifications()
	* cancelNotification (String pkg, String tag, int id)
	* getActiveNotifications()
2. StatusBarNotification
	* getId
	* getNotification
	* getPackageName
	* getPostTime
	* isClearable
	* isOngoing
``` java

Bundle extras = sbn.getNotification().extras;
String notificationTitle = extras.getString(Notification.EXTRA_TITLE);
Bitmap notificationLargeIcon = ((Bitmap)extras.getParcelable(Notification.EXTRA_LARGE_ICON));
Bitmap notificationSmallIcon = ((Bitmap)extras.getParcelable(Notification.EXTRA_SMALL_ICON));
CharSequence notificationText = extras.getCharSequence(Notification.EXTRA_TEXT);
CharSequence notificationSubText = extras.getCharSequence(Notification.EXTRA_SUB_TEXT);

```

## Note
First running will show a dialog to enable "Notification access", choose "OK" to continue.
Manual: "Settings > Security > Notification access".

## License
Copyright 2014 gitonway.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.


[1]: https://github.com/kpbird/NotificationListenerService-Example
[2]: http://developer.android.com/reference/android/service/notification/NotificationListenerService.html
[3]: https://github.com/yihongyuelan/NotificationListenerServiceDemo/blob/master/screenshot/SevenNLS00.gif
[4]: https://github.com/yihongyuelan/NotificationListenerServiceDemo/blob/master/screenshot/SevenNLS01.gif

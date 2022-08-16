-
- |||System notification|hasNotificationPermission|pushDisabled|subscribed|notificationPermissionStatus|
  |--|--|--|--|--|--|--|
  |Android|11 RKQ1.200826.002|off|false|true|false|null|
  |Android|11 RKQ1.200826.002|on|true|false|true|null|
  |iOS||off|||||
  |iOS||on|||||
-
- ## Record
- ### Android
- 1. delete existing app
  2. install
  3. 
  ```dart
  OneSignal.shared.setLogLevel(OSLogLevel.verbose, OSLogLevel.none);
  OneSignal.shared.setAppId(EnvConfig.oneSignalAppID);
  ```
  4. `OneSignal.shared.setSubscriptionObserver` triggered
  ![image.png](../assets/image_1660621311388_0.png){:width 300, :height 265}
- 5. `OneSignal.shared.setSubscriptionObserver` triggered again
  ![image.png](../assets/image_1660621536789_0.png){:width 300, :height 265}
- 6. 
  ```
  OneSignal.*shared*.promptUserForPushNotificationPermission().then((accepted) {
  // accepted = false
  });
  ```
- 7. go to setting page
  8. ` OneSignal.shared.getDeviceState()`
  ![image.png](../assets/image_1660621748611_0.png){:width 300, :height 265}
- 9. close app and go to setting **turn off** notification permission
  10. reopen app
  11. 
  ```dart
  OneSignal.shared.setLogLevel(OSLogLevel.verbose, OSLogLevel.none);
  OneSignal.shared.setAppId(EnvConfig.oneSignalAppID);
  ```
- 12. 
  ```dart
  OneSignal.shared.promptUserForPushNotificationPermission().then((accepted) {
  	// accepted = false
  });
  ```
- 12. go to setting page
  13. 
  ```dart
  OneSignal.shared.getDeviceState()
  ```
  ![image.png](../assets/image_1660623596994_0.png){:width 300, :height 265}
  14. `OneSignal.shared.setSubscriptionObserver` triggered
  ![image.png](../assets/image_1660622531311_0.png){:width 300, :height 265}
- 15. now push notification is **off** in ui
  16. click `on` in ui
  ```
  OneSignal.*shared*.disablePush(*true*);
  ```
- ```
  OneSignal.*shared*.setSubscriptionObserver
  ```
- ![image.png](../assets/image_1660623808500_0.png){:width 300, :height 265}
- 17. back and open setting again
  ````
  OneSignal.*shared*.getDeviceState()
  ````
  ![image.png](../assets/image_1660623917997_0.png){:width 300, :height 265}
-
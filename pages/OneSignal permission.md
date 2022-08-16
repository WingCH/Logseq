-
- |||System notification||
  |--|--|--|--|
  |Android|11 RKQ1.200826.002|off||
  |Android|11 RKQ1.200826.002|on||
  |iOS||off||
  |iOS||on||
-
- ## Record
- ### Android
- 1. delete old app
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
  OneSignal.*shared*.promptUserForPushNotificationPermission().then((accepted) {});
  ```
- 7. go to setting page
  8. ` OneSignal.shared.getDeviceState()`
  ![image.png](../assets/image_1660621748611_0.png){:width 300, :height 265}
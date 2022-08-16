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
  ```
  OneSignal.shared.setLogLevel(OSLogLevel.verbose, OSLogLevel.none);
  OneSignal.shared.setAppId(EnvConfig.oneSignalAppID);
  ```
  5. ``OneSignal.shared.setSubscriptionObserver trigger
  ![image.png](../assets/image_1660621311388_0.png)
-
-
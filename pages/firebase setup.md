- dou't use firebase CLI, because cannot support Analytics / Crashlytics
-
- ## GTM
- ### Android
- 1. download GTM json and put it into `android/app/src/{flavor}/assets/containers/GTM-M98R8HQ.json`
  2.  add `implementation 'com.google.android.gms:play-services-tagmanager:18.0.1'` into `android/app/build.gradle`
  3. you can see following log in logcat if success 
  ```
  I/GoogleTagManager: Loading container GTM-MXXXXXX
  I/GoogleTagManager: Installing Tag Manager event handler.
  I/GoogleTagManager: Tag Manager event handler installed.
  I/GoogleTagManager: Tag Manager initilization took 2ms
  ```
-
- ### iOS
- 1. follow step 1 to 4
  https://developers.google.com/tag-platform/tag-manager/ios/v5
- 2. test in **Simulator**
  ```
  07-06 12:50:45.397125+0800 Runner[22387:3414875] GoogleTagManager info: Loading container: GTM-KM7V4TH
  2022-07-06 12:50:46.020878+0800 Runner[22387:3414865] GoogleTagManager info: Attempting to load saved version of container GTM-KM7V4TH
  2022-07-06 12:50:55.533238+0800 Runner[22387:3414921] GoogleTagManager info: Processing logged event: gtm.load with parameters: (null)
  2022-07-06 12:50:55.723183+0800 Runner[22387:3414921] GoogleTagManager info: Processing logged event: _vs with parameters: {
  ```
-
-
-
-
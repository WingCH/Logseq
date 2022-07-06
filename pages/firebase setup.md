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
- 1. download GTM json and put it into
-
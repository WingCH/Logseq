- dou't use firebase CLI, because cannot support Analytics / Crashlytics
-
- ## GTM
- ### Android
- 1. download GTM json and put it into `android/app/src/{flavor}/assets/containers/GTM-M98R8HQ.json`
  2.  add `implementation  implementation 'com.google.android.gms:play-services-tagmanager:18.0.1'` into `android/app/build.gradle`
  3. if success you can see
  ```
  I/GoogleTagManager: Loading container GTM-M98R8HQ
  I/GoogleTagManager: Installing Tag Manager event handler.
  
  ```
-
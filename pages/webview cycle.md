- package: [flutter_inappwebview](https://pub.dev/packages/flutter_inappwebview)
- source code: [flutter_inappwebview_video_study](https://github.com/WingCH/Learning/tree/main/Flutter/flutter_inappwebview_video_study)
- web sample: https://video-webview-sample.pages.dev
- ## Normal case example
- ### code:
- {{renderer :linkpreview,https://github.com/WingCH/Learning/blob/5faee74255eb24a18b2bddcbb7aebe74f613a985/Flutter/flutter_inappwebview_video_study/lib/main.dart}}
- ### Result:
- Step:
- 1. onUpdateVisitedHistory
  2. onLoadStart
  3. onProgressChanged until 100%
  4. onLoadStop
- ![image.png](../assets/image_1659840345765_0.png)
- ---
- ## Video example
- ## iOS
- ### Step: (preview enabled)
- #### dart side: (10:49:56.278666 to 10:50:10.716124) = ~14s
	- 1. onLoadStart (10:49:56.278666)
	  2. onProgressChanged until 100% (10:49:56.294044 to 10:50:10.715166)
	  3. onLoadStop (10:50:10.716124)
- #### web side:
	- 1. start (10:49:56.454968)
	  2. body onload event trigger (10:50:10.719071)
- ![image.png](../assets/image_1659840706806_0.png)
- #### Tried 5 times (preview enabled)
- ```dart
  mediaPlaybackRequiresUserGesture = false
  ```
- 1. 11:28:12.723413 to 11:28:16.683238 = ~4s
  2. 11:29:30.897574 to 11:29:34.691882 = ~4s
  3. 11:30:29.345046 to 11:30:29.591031 = ~0.5s
  4. 11:31:23.764104 to 11:31:27.060416 = ~4s
  5. 11:32:12.898111 to 11:32:16.15298 = ~4s
-
- #### Tried 5 times (preview disabled)
- ```dart
  mediaPlaybackRequiresUserGesture = true
  ```
- 1. 11:34:05.413464 to 11:34:05.563590 = ~0.1s
  2. 11:36:06.613571 to 11:36:06.810674 = ~0.2s
  3. 11:37:57.900841 to 11:37:58.058672 = ~0.7
  4. 11:38:34.508078 to 11:38:34.660268 = ~0.2s
  5. 11:39:07.133079 to 11:39:07.309460 = ~0.2s
- ## Android
### Step:
- #### dart side: (11:16:49.683851 to 11:16:50.926373)
	- 1. onLoadStart (11:16:49.683851)
	  2. onProgressChanged until 100% (11:16:49.630229 to 11:16:50.914226)
	  3. onLoadStop (11:16:50.926373)
- #### web side:
	- 1. start (11:16:49.705529)
	  2. body onload event trigger (11:16:50.926373)
- ![image.png](../assets/image_1659842262171_0.png)
- #### Tried 5 times (preview seems cannot disable)
- ```
  mediaPlaybackRequiresUserGesture = true/false
  ```
- 1. 11:44:34.596762 to 11:44:34.998641 =~0.4s
  2. 11:45:36.173198 to 11:45:36.582592 =~0.4s
  3. 11:46:23.959169 to 11:46:24.234121 =~0.3s
  4. 11:47:13.573164 to 11:47:13.987937 =~0.4s
  5. 11:47:51.159277 to 11:47:51.363543 =~0.2s
-
- ---
- ## Conclusion
- Now in order to display the thumbnail of the video, we need to preload video , but it takes few seconds or more on the ios side.
- #### Solution
- backend prepares the thumbnail of the video, so that the frontend does not need to obtain the thumbnail through preload
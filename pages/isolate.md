- with isolate
	- ```
	  flutter: processImage executed in 0:00:05.826857
	  [ServicesDaemonManager] interruptionHandler is called. -[FontServicesDaemonManager connection]_block_invoke
	  flutter: removeBackground start
	  flutter: getBytes executed in 0:00:00.000281
	  flutter: removedBackgroundImage executed in 0:00:00.038921
	  flutter: imageToImagePixelBytes encodePng executed in 0:00:02.500106
	  flutter: removeBackground executed in 0:00:12.643845
	  ```
- without isolate
	- ```
	  flutter: processImage executed in 0:00:05.602216
	  flutter: removeBackground start
	  flutter: getBytes executed in 0:00:00.000247
	  flutter: removedBackgroundImage executed in 0:00:00.036195
	  flutter: imageToImagePixelBytes encodePng executed in 0:00:02.453975
	  flutter: removeBackground executed in 0:00:08.613088
	  ```
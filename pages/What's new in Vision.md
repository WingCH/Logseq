- NEW: Person segmentation (人物分割)
  collapsed:: true
	- ![image.png](../assets/image_1654999973081_0.png){:height 360, :width 491}
- NEW: hand pose estimation (手勢估計)
  collapsed:: true
	- ![image.png](../assets/image_1654999958456_0.png)
- Text recognize
  collapsed:: true
	- best : specify languages to vision, leave automatically DetectsLanguage turned off
	- spoort 韓文
- New ML-based **barcode** detector and decoder
	- Faster for multiple codes — "constant time"
	- VNDetectBarcodesRequestRevision3
	- VNDetectBarcodesRequestRevision2 vs VNDetectBarcodesRequestRevision3
		- VNDetectBarcodesRequestRevision2
			- ![image.png](../assets/image_1655001951874_0.png){:height 326, :width 215}
			- 1. missing first barcode
			  2. detected the second barcode twice
			  3. a line through the barcode rather than complete bounding box.
		- VNDetectBarcodesRequestRevision3
			- ![image.png](../assets/image_1655002257925_0.png){:height 394, :width 412}
			-
- New ML-based optical flow generator
  collapsed:: true
	- ![image.png](../assets/image_1655001001732_0.png){:height 265, :width 499}
	- video object track use
- Face Landmarks
	- VNDetectFaceLandmarksRequestRevision3
	- Xcode support quick look to see face landmark
		- ![image.png](../assets/image_1655001610853_0.png){:height 310, :width 610}
		- if image is already release in memory, debug tool can still generate below image
			- ![image.png](../assets/image_1655001775550_0.png){:height 233, :width 616}
- quick look
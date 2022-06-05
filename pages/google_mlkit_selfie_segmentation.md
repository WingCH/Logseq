title:: google_mlkit_selfie_segmentation

- ![id_photo.jpg](../assets/id_photo_1654426412190_0.jpg){:height 299, :width 548}
- size: 2048*1365
- ```dart
  _segmenter = SelfieSegmenter(
    mode: SegmenterMode.single,
    enableRawSizeMask: false,
  );
  
  ...
  
  Stopwatch stopwatch =  Stopwatch()..start();
  final SegmentationMask? mask = await _segmenter.processImage(inputImage);
  print('executed in ${stopwatch.elapsed}');
  ```
- pixel 6 in profile mode: `executed in 0:00:02.873917`
-
-
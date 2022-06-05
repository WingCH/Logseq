- {{renderer :linkpreview,https://gist.github.com/plateaukao/ebb5e7169dd89cc52bda338762d4997e}}
-
- ## Issue
- Why pass by reference #issue
- ```dart
    Future<image_library.Image?> colorTransparent(
        image_library.Image src, int red, int green, int blue) async {
      // TODO: why pass by reference
      Uint8List pixels = src.getBytes();
      for (int i = 0, len = pixels.length; i < len; i += 4) {
        if (pixels[i] == red && pixels[i + 1] == green && pixels[i + 2] == blue) {
          // convert to color red
          pixels[i] = 229;
          pixels[i + 1] = 57;
          pixels[i + 2] = 53;
        }
      }
      return src;
    }
  ```
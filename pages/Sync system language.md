- iOS settings no display app setting item before adding `Localizations` in xcode #iOS #xcode
  collapsed:: true
	- default `Localizations` setting
	- ![image.png](../assets/image_1655287401953_0.png)
- When set `Localizations` once in xcode, iOS
-
- Case 1
	- Example project not set any Localization in Xcode
		- ![image.png](../assets/image_1655284191132_0.png)
	- Simulator 語言與地區
		- 語言: 繁體中文
		- 地區: 香港
		- ![image.png](../assets/image_1655284278188_0.png){:height 563, :width 311}
	- Use `AppleLanguages` get user default
		- ```swift
		  UserDefaults.standard.array(forKey: "AppleLanguages")
		  // [ "zh-Hant-HK" ]
		  ```
-
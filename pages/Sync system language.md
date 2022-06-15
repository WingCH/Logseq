- Case 1
	- Example project not set any Localization in Xcode
	  collapsed:: true
		- ![image.png](../assets/image_1655284191132_0.png)
	- Simulator 語言與地區
	  collapsed:: true
		- 語言: 繁體中文
		- 地區: 香港
		- ![image.png](../assets/image_1655284278188_0.png){:height 563, :width 311}
	- Use `AppleLanguages` get user default
	  collapsed:: true
		- ```swift
		  UserDefaults.standard.array(forKey: "AppleLanguages")
		  // [ "zh-Hant-HK" ]
		  ```
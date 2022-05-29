- # Requirement
- 1. The height of the white container is based on the size of the text widget
  2. White containers in the same row need to be the same height
- [[draws/2022-05-28-10-05-29.excalidraw]]
- ## Problem:
- White containers in the same row do not know the size of other white containers
- |||
  |--|--|
  | ![image.png](../assets/image_1653795799275_0.png) | ![image.png](../assets/image_1653795812985_0.png) |
- |||
  |--|--|
  | ![image.png](../assets/image_1653801797787_0.png) | ![image.png](../assets/image_1653801766079_0.png) |
- |||
  |--|--|
  | ![image.png](../assets/image_1653801863357_0.png) | ![image.png](../assets/image_1653801874428_0.png) |
- <p>There is an error with your mermaid syntax. Please rectify and render again.</p>
  {{renderer :mermaid_ekqyyhu}}
	- ```mermaid 
	  flowchart TB
	      Container-->|`BoxConstraints(w=250.0, 0.0<=h<=Infinity)`|B
	  ```
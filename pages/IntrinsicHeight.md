- # Requirement
- 1. The height of the white container is based on the size of the text widget
  2. White containers in the same row need to be the same height
- [[draws/2022-05-28-10-05-29.excalidraw]]
- ## Problem:
- White containers in the same row do not know the size of other white containers
- |||
  |--|--|
  | ![image.png](../assets/image_1653795799275_0.png) | ![image.png](../assets/image_1653795812985_0.png) |
-
- <img src="https://mermaid.ink/img/ICBmbG93Y2hhcnQgVEIKICAgIEEK" />
  {{renderer :mermaid_qzitkrejb}}
	- ```mermaid 
	  gantt
	      title A Gantt Diagram
	      dateFormat  YYYY-MM-DD
	      section Section
	      A task           :a1, 2014-01-01, 30d
	      Another task     :after a1  , 20d
	      section Another
	      Task in sec      :2014-01-12  , 12d
	      another task      : 24d
	  ```
-
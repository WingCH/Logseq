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
- <img src="https://mermaid.ink/img/ICAgICAgZ2l0R3JhcGgKICAgICAgIGNvbW1pdAogICAgICAgY29tbWl0CiAgICAgICBicmFuY2ggZGV2ZWxvcAogICAgICAgY2hlY2tvdXQgZGV2ZWxvcAogICAgICAgY29tbWl0CiAgICAgICBjb21taXQKICAgICAgIGNoZWNrb3V0IG1haW4KICAgICAgIG1lcmdlIGRldmVsb3AKICAgICAgIGNvbW1pdAogICAgICAgY29tbWl0Cg" />
  {{renderer :mermaid_qzitkrejb}}
	- ```mermaid 
	      gitGraph
	         commit
	         commit
	         branch develop
	         checkout develop
	         commit
	         commit
	         checkout main
	         merge develop
	         commit
	         commit
	  ```
-
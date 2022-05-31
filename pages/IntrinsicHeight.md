- # Requirement
- 1. The height of the white container is based on the size of the text widget
  2. White containers in the same row need to be the same height
- [[draws/2022-05-28-10-05-29.excalidraw]]
- ## Problem:
- White containers in the same row do not know the size of other white containers
- |||
  |--|--|
  | ![image.png](../assets/image_1653795799275_0.png) | ![image.png](../assets/image_1653795812985_0.png) |
- <img src="https://mermaid.ink/img/ICBncmFwaCBURAogICAgU2NhZmZvbGQgLS0-IHwiQm94Q29uc3RyYWludHMoMC4wPD13PD0xMTgwLjAsIDAuMDw9aDw9NzE2LjApInwgcm9vdAogICAgcm9vdFtDb250YWluZXJdOjo6dGVhbENvbG9yIC0tPiB8IkJveENvbnN0cmFpbnRzKHc9MjUwLjAsIDAuMDw9aDw9NzE2LjApInxSb3cKICAgIFJvdyAtLT4gIEl0ZW0xCiAgICBSb3cgLS0-ICBJdGVtMgogICAgUm93IC0tPiBJdGVtMwogICAgSXRlbTIgLS0-IHwiQm94Q29uc3RyYWludHMoMC4wPD13PD1JbmZpbml0eSwgMC4wPD1oPD03MTYuMCkifCBDb2x1bW4gCiAgICBDb2x1bW4gLS0-IHRleHRDb250YWluZXJbQ29udGFpbmVyXSAtLT4gVGV4dCAtLT4gfCJTaXplKDc2LjAsIDE2LjApInwgdGV4dENvbnRhaW5lcltDb250YWluZXJdIC0tPnwiU2l6ZSg3Ni4wLCAxNi4wKSJ8IENvbHVtbgogICAgQ29sdW1uIC0tPiBmaXhDb250YWluZXJbQ29udGFpbmVyXSAtLT4gfCJCb3hDb25zdHJhaW50cyh3PTUwLjAsIGg9MTAwLjApInwgQ29sdW1uCiAgICAKICAgIGNsYXNzRGVmIHRlYWxDb2xvciBmaWxsOiMwMDk2ODg7Cg" />
  {{renderer(:mermaid_ekqyyhu)}}
	- ``` mermaid 
	  	  graph TD
	  	      Scaffold --> |"BoxConstraints(0.0<=w<=1180.0, 0.0<=h<=716.0)"| root
	  	      root[Container]:::tealColor --> |"BoxConstraints(w=250.0, 0.0<=h<=716.0)"|Row
	  	      Row -->  Item1
	  	      Row -->  Item2
	  	      Row --> Item3
	  	      Item2 --> |"BoxConstraints(0.0<=w<=Infinity, 0.0<=h<=716.0)"| Column 
	  	      Column --> textContainer[Container] --> Text --> |"Size(76.0, 16.0)"| textContainer[Container] -->|"Size(76.0, 16.0)"| Column
	  	      Column --> fixContainer[Container] --> |"BoxConstraints(w=50.0, h=100.0)"| Column
	  	      
	  	      classDef tealColor fill:#009688;
	  ```
	-
- |||
  |--|--|
  | ![image.png](../assets/image_1653801797787_0.png) | ![image.png](../assets/image_1653801766079_0.png) |
- |||
  |--|--|
  | ![image.png](../assets/image_1653801863357_0.png) | ![image.png](../assets/image_1653801874428_0.png) |
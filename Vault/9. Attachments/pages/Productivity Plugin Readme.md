## Kanban
collapsed:: true
	- tag a block with `#.v-kanban` or `#.v-kanban-wide` (more samples here [https://discuss.logseq.com/t/css-trigger-columns-kanban-view-with-tags/390](https://discuss.logseq.com/t/css-trigger-columns-kanban-view-with-tags/390 "undefined")) - - see the related Template below
		- options:
			- `-w100`, `-w150`, `-w200`, `-w300`,`-w400` : adjust width of each column (fixed numbers in px)
			- `-small` : smaller fonts to fit more columns
			- `-wide` : force the use of full-width and horizontal scroll if needed demo: `#.v-kanban`
				- ![](https://user-images.githubusercontent.com/4605693/156956422-9eab8cee-7fbb-4e65-81de-5097c1b96f89.png)
		- Kanban starter templates: replace the titles and catagories to your liking, invoke with `/kanban````
			- - a Kanban #.v-kanban
			- template:: kanban
				- - `TO DO`
					- - 1
					- - 2
				- - `IN PROGRESS`
					- - 1
					- - 2
				- - `DONE`
					- - 1
					- - 2
			- - Wide Kanban #.v-kanban-wide
			- template:: kanban-wide
				- - `UNDER REVIEW`
					- - 1
					- - 2
				- - `RETAKE`
					- - 1
					- - 2
				- - `APPROVED`
					- - 1
					- - 2
				- - `ARCHIVED`
					- - 1
					- - 2
				- - `DROPPED`
					- - 1
					- - 2
			- ## Eisenhower Matrix
			  tag a block with `#.v-eisenhower` ([https://discuss.logseq.com/t/css-template-eisenhower-matrix/526](https://discuss.logseq.com/t/css-template-eisenhower-matrix/526 "undefined"))
			  Priority Matrix `#.v-eisenhower-matrix`  
			  ![](https://user-images.githubusercontent.com/4605693/156956223-a9cf13d8-4aa5-4f17-9726-9f5c5a49a3f7.png)
			  use this template for easy invoke via slash command `/eisenhower-matrix` :```
				- #.v-eisenhower-matrix
				  template:: eisenhower-matrix
					- [[TODO]]
						-
						-
						-
					- [[DECIDE]]
						-
						-
						-
					- [[DELEGATE]]
						-
						-
						-
					- [[ELIMINATE]]
						-
						-
						-
			- ```
			  ```
- ## Numbered lists
	- tag a block with `#.v-numlist` ([https://discuss.logseq.com/t/css-numbered-lists/387/5](https://discuss.logseq.com/t/css-numbered-lists/387/5 "undefined")) to repace children bullets with incremental numbers (works on 2 sub-levels max for now) ![](https://user-images.githubusercontent.com/4605693/157914206-e1220ef0-e14e-47b8-8ded-d86aa5a422b8.png)
- ## Border
	- a utility tag to create borders around blocks. use `#.v-self-border`; `#.v-border-child` or `#.v-self-border-child` to add a frame/border around blocks. Great to highlight important blocks or to make cards or tables with the kanban or columns tags
	- demo : ![](https://user-images.githubusercontent.com/4605693/156955395-0004e961-4d18-4dc8-9621-8b4168c91b05.png)
- ## Gallery
	- tag a parent block with `#.v-gallery` and put links to images in separate children blocks (by default the images are displayed as 200x200px)
		- options:
			- `-col2` to `-col7` : defnine the number of columns, images size will auto adjust
			- `-w100`, `-w200`, `-w300`,`-w400` : adjust width of each pic (fixed numbers in px)
			- `-fit` : fit width
			- `-h300` or `-h400` to change the height, default is 200px
			- append these suffixes to the main tag, so for instance : `#.v-gallery-col5` creates a grid of 5 columns, `#.v-gallery-w300` creates a gallery where each pic is 300 pixels wide, etc
		- demo: `#.v-gallery-fit` ![](https://user-images.githubusercontent.com/4605693/156956622-fc96e39a-4240-4c22-a4e2-a37cd7b75126.png)
- ## Like-Dislike (Pro-Cons)
	- tag a bock with `#like` or `#dislike` for reviews or comparisons: it will replace the bullets by `+` and `-` . see the related Template below demo `#Like` and `#Dislike` (with #.v-kanban applied)
	- ![](https://user-images.githubusercontent.com/4605693/156959797-88fbfbeb-fd02-48fb-9e4e-6a72974a1f24.png)
		- pros and cons template(used for reviews or comparisons, works well in conjunction with the #.v-kanban tags)```
			- - procons #.v-kanban
			- template:: procons
				- - #like
					- -
				- - #dislike
					- -
-
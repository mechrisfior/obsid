# Daily
template:: My Day, Daily Agenda
collapsed:: true
	- ###  ^^Critical Tasks for Today^^
	  			{{query (task TODO DOING LATER)}}
	  query-table:: true
	- ### ^^#Log^^
	- ### Notes
	- ### Meetings
		- 07:00
		- 08:00
	- ### Active Projects
	- **Floating Ideas** {{query [[log/ideas]]}}
	  query-table:: true
	  query-properties:: [:block]
		- query-table:: true
		  query-properties:: [:block]
		-
	- ### What did I do for ME today?
		-
		-
- # Weekly Review
  template:: WeeklyReview
  collapsed:: true
	- ### A line about this week
	- ### A line about today
	- ### What went well this week?
	- ### What needs improvement?
	- ### What could I have spent more or less time doing?
	- ### What am I grateful for this week?
	- ### What am I proud of this week?
	- ### What brought me joy this week?
	- ### What did I learn?
	- ### What #[[goals]] did I work towards?
	- ### What goals will I focus on next week?
- Query tasks on this page Template
  template:: page tasks
  template-including-parent:: false
  collapsed:: true
	- {{query (and (todo todo doing) (page <% current page %>))}}
	  collapsed:: true
- ### Weekdays and Holidays (Templates)
  comment:: Always turn on Weekdays and holidays (Templates) plugin for execute rendering when journal template is called.
  collapsed:: true
  [English document](https://github.com/YU000jp/logseq-plugin-weekdays-and-weekends/wiki/English-document)
	- #### Journal: Template Settings
	  template:: Journal
	  template-including-parent:: false
	  comment:: Edit config.edn `:default-templates {:journals "Journal"}` When load as journal template, the renderings are executed. During runtime, the block with renderings be removed. A block can have a maximum of seven renderings, but if the weekdays overlap, only one of them will be executed.
	  background-color:: yellow
	  collapsed:: true
		- #### AM
			-
			-
		- #### PM
			-
			-
		-
	- #### Main-Template:
	  template:: Main-Template
	  template-including-parent:: false
	  background-color:: gray
		- #### AM
			-
			-
		- #### PM
			-
	- #### Sub-Template:
	  template:: Sub-Template
	  template-including-parent:: false
	  background-color:: gray
	  collapsed:: true
		- #### AM
			-
			-
		- #### PM
			-
			-
	- #### Weekends-Template:
	  template:: Weekends-Template
	  template-including-parent:: false
	  background-color:: gray
	  collapsed:: true
		- #### AM
			-
			-
		- #### PM
			-
			-
	- #### Holidays-Template:
	  template:: Holidays-Template
	  template-including-parent:: false
	  background-color:: gray
	  collapsed:: true
		- #### AM
			-
			-
		- #### PM
			-
			-
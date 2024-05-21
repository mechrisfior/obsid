date:: [[Oct 17th, 2023]] 
template:: Meetings 👥

	- query-table:: true
	  query-sort-by:: block
	  query-sort-desc:: false
	  #+BEGIN_QUERY
	  {:title [:b "Meeting referencing 🔎" ]
	  :query  [:find (pull ?b [*])
	  :in $ ?end ?daysback
	  :where
	  [?b :block/path-refs ?ref]
	  (not [?b :block/page ?page]           ;<--- :block/page is an id,
	  [?page :block/name "meetings"])       ;     not a string
	  [?ref :block/name "meetings"]
	  [?b :block/created-at ?v]
	  [(* ?daysback 60 60 24 1000) ?range]
	  [(- ?end ?range) ?period]
	  [(>= ?v ?period)]
	  [(< ?v ?end)]
	  ]
	  :inputs [:end-of-today-ms 8]
	  :result-transform (fn [result]
	                 (sort-by (fn [h]
	                            (get h :block/updated-at)) result))
	  }
	  #+END_QUERY
	- ## **To ask:**
		- Are we gonna be able to sell Mega Messenger as personal frontend ?
			- Kinda, But Why Not use the Mega Link?
		- What about using prelander + finance survey -> Magic Link on Propellerads with Push and Pop ads / pop unders?
		- {{embed ((652e8089-2458-4164-a9bb-9513642a327c))}}
		-
	- ## To-Do
	- ## Key points
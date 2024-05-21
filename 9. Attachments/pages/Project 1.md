- /
- date:: 
  template:: Meetings 👥
  people::
	- #+BEGIN_QUERY
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
	- ## To-Do
	- ## Key points
tags:: project page
icon:: 📂

-
- ### Project Meta
  id:: 65201041-bac2-4cdc-9be1-b6562561e5ad
	- DONE #project [[#OLSP Academy]]
	- query-table:: false
	  #+BEGIN_QUERY
	  {:title [:h4 "Tasks related to [[OLSP Academy]]"]
	  :query [:find (pull ?b [*])
	       :in $ ?current-page
	       :where
	       [?p :block/name ?current-page]
	       [?b :block/marker ?marker]
	  [?p :block/alias ?al]
	  (or [?b :block/refs ?p] [?b :block/refs ?al])
	  (or
	       [(= "NOW" ?marker)]
	       [(= "DOING" ?marker)]
	       [(= "WAITING" ?marker)]
	       [(= "LATER" ?marker)]
	  )
	  (not [?b :block/page ?p])
	  ]
	  :inputs [:current-page]
	    :result-transform (fn [result]
	                        (sort-by (fn [b]
	                                   (get b :block/priority "Z")) result))
	    :breadcrumb-show? false
	    :table-view? false
	  }
	  #+END_QUERY
	- query-table:: false
	  #+BEGIN_QUERY
	  {:title [:h4 "Checklist"]
	  :query (and (todo todo) (page [[OLSP Academy]]))
	    :result-transform (fn [result]
	                        (sort-by (fn [b]
	                                   (get b :block/priority "Z")) result))
	    :breadcrumb-show? false
	    :table-view? false
	  }
	  #+END_QUERY
- ### Notes
	- [[VIP Onboarding Call on [[Oct 2nd, 2023]] ]]
	  id:: 6c1aaf44-54ff-4e72-8982-cc66d3f1dc09
	-
-
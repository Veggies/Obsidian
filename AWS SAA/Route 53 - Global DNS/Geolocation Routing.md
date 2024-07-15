Records are tagged with location
	Country, continent, or default
Doesn't return closest records
	Returns relevant records
		State, country, then continent
			If any matches occur, the record is returned and stopped.
				Matches one state, then matches country, then continent.
	If no relevant records, NO ANSWER response
Use Case:
	Regional Restrictions
	Load balancing across regional endpoints
### User defined extensions
Extensions to the openGEDCOM spec can easily be accomplished by creating a new tag or attribute beginning with an underscore.

**Example**
{
	"_LDS": [
		"baptism": {
			"date": "7 APR 1982",
			"temple": "CHICA",
			"status": "completed"
		},
		"endowment": {
			"date": "7 APR 1982",
			"temple": "CHICA",
			"status": "cleared"
		},
		"sealingChild": {
			"date": "7 APR 1982",
			"temple": "CHICA",
			"status": "completed"
			"participants": [
				{
					"role": "father",
					"ref": "IN001"
				},
				{
					"role": "child",
					"ref": "IN003"
				}
			]
		},
		"sealingSpouse": {
			"date": "7 APR 1982",
			"temple": "CHICA",
			"status": "cleared"
			"participants": [
				{
					"role": "husband",
					"ref": "IN001"
				},
				{
					"role": "wife",
					"ref": "IN002"
				}
			]
		},
	]
}
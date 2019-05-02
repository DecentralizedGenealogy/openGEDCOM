# Cousin List
This is a proposed rough draft of a standardized way of representing a list of cousins. A common use case is representing a set of cousins found through DNA testing. Another use case is representing a set of cousins found through a common share Family Tree service.

```
{
    "cousinList": {
        "creator": {
			"name": "Bob Jones",
            "email": "bob@example.com",
			"url": "http://example.com/familyarchive",
            "date": "April 1, 2019"
        },
        "serviceProvider": [
            "23andme": {
                "date": "Date list was created",
                "cousins": [
                    {
                        "name": "Jane Wilson",
                        "realtionship": "4th cousin twice removed",
                        "contact": {
                            "email": "jane@example.com",
                            "url": "https://23andme.com/users/jane",
                            "phone": "702-555-1212"
                        }
                    },
                    {...}
                ]
            },
            "ancestry": {
                "date": "Date list was created",
                "cousins": [
                    {
                        "name": "Sally Brown",
                        "realtionship": "6th cousins",
                        "contact": {
                            "email": "sally@example.com",
                            "url": "https://ancestry.com/profile/sally",
                            "phone": "800-555-1212"
                        }
                    },
                    {...}
                ]
            }
        ]
    }
}
```
# Family Archive
This is proposed rough draft of how a Family Archive could be represented in a standardized way. A Family Archive is a container of digital assets related to a family organization. It's flexible enough to contain any digital media you want in a structured standardized way. Thus, allowing the archive to be portable between service providers, and avoid vender lockin.
```
{
	"familyarchive": [
        "creator": {
			"name": "Bob Jones",
            "email": "bob@example.com",
			"url": "http://example.com/familyarchive"
        },
        "contents": [
            "photos": [],
            "documents": [],
            "tree": [],
            "video": [],
            "audio": [],
            "other": []
        ],
        {...}
    ]
}
```
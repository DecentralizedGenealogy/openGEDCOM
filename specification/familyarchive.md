# Family Archive
This is proposed rough draft of how a Family Archive could be represented in a standardized way. A Family Archive is a container of digital assets related to an individual, family, or organization. It's flexible enough to contain any digital media you want in a structured standardized way. Thus, allowing the archive to be portable between service providers, and avoid vender lock-in.

All fully qualified URIs contained in a Family Archive must be long lived and the hosting provider must make an effort to maintain the links forever (or redirect to equivalent URI), to claim compatability with the Family Archive standard.

```
{
    "archive": [
        "creator": {
            "name": "Bob Jones",
            "email": "bob@example.com",
            "url": "http://example.com/familyarchive"
        },
        "contents": [
            "photos": [ {...} ],
            "documents": [ {...} ],
            "tree": [ {...} ],
            "video": [ {...} ],
            "audio": [ {...} ],
            "other": [ {...} ],
        ],
        {...}
    ]
}
```
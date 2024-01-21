---
up: "[[Sources MOC]]"
tags:
  - "#map/view"
created: 2023-12-13T11:55
updated: 2024-01-15T14:20
---

> [!HINT]+ ReadItLater Sources
> 

## YouTube Videos
```dataview
TABLE WITHOUT ID
	file.link as "File Name", tags as "Tags", sourceStatus as "Status", file.mday as "Last Modified", (date(today) - file.cday).day as "Days alive"
FROM "Sources/ReadItLater_Inbox" 
WHERE contains(file.name, "Youtube")
SORT (date(today) - file.cday).day DESC
```

## Tweets
```dataview
TABLE WITHOUT ID
	file.link as "File Name", tags as "Tags", sourceStatus as "Status", file.mday as "Last Modified", (date(today) - file.cday).day as "Days alive"
FROM "Sources/ReadItLater_Inbox" 
WHERE contains(file.name, "Tweet")
SORT (date(today) - file.cday).day DESC
```

## Articles
```dataview
TABLE WITHOUT ID
file.link as "File Name", tags as "Tags", sourceStatus as "Status", file.mday as "Last Modified", (date(today) - file.cday).day as "Days alive"
FROM "Sources" 
WHERE type = "article"
SORT (date(today) - file.cday).day DESC
```

---
up:
  - "[[+00 Y2024-Metrics]]"
created: 2024-01-02T10:55
updated: 2024-01-19T08:21
---


```dataview
TABLE
	AZ_Rise as "⏰", 
	Suryanamaskar as "🌞",
	Meditation as "🧘‍♂️", 
	Workout as "🏋️", 
	week-note as "📆",
	AZ_Set as "🛌",
	(AZ_Set - AZ_Rise) as "Sleep"
FROM "Calendar/Y2024/01 Daily Notes" 
WHERE contains(AZ_Rise,"AM") 
SORT file.name DESC
```

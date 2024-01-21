---
up:
  - "[[🏠 Home]]"
  - "[[Plan and Review]]"
tags:
  - "#map/view"
same:
  - "[[Weekly Notes]]"
created: 2023-12-13T11:55
updated: 2024-01-01T10:30
---

# Daily Notes

A daily note practice is great for many people. Try it out. ==Just never feel obligated to make a daily note every day. But do use them.== They are great for a mixture of uses, such as: 

- Tracking Habits or Important Metrics
- Jotting down ideas
- Planning My Day 
- Taking Logs of what I am doing and done today
- Reflecting on My day

Understanding Daily Note format and purpose of each section.

| Sr | Heading | Content | Purpose | When To Use | Nature |
| ---- | ---- | ---- | ---- | ---- | ---- |
| 1 | Time Blocks Statistics | Contains Time Blocks of 10 minutes | Just Look at it to know how many T10 Blocks are remaining. | During Whole Day | Read Only |
| 2 | Health Metrics | - Morning Routine<br>- Food Journal | This creates a tracker for Important Health and Habit Metrics | Morning | Write |
| 3 | Notes | - Logs<br>- Tasks<br>- Quick Capture (Mobile) | Contains Daily Logs, Ideas, Thoughts, etc.<br>Use it During Day time. | During Day | Write |
| 4 | Day Review | - Mood Journal<br>- Evening Routine | It helps to be mindful about my moods and sets responsibility for effective Evening Routine. | Evening | Write |
| 5 | Note Statistics | - Notes Created<br>- Notes Modified | This gives clue about how many notes I created or modified. It helps in Evening Reflection. | Evening | Read Only |

The only things I have found I care to log consistently I have given tags:

- #Log/event 
- #Log/journal 
- #Log/meeting

While I prefer to click on the Calendar (over in the upper right usually), below is a simple view of the latest daily notes—including a few from the future:

```dataview
TABLE file.mtime as "Last Modified Date", tags As "File Type", week-note as "Week Note"
FROM "Calendar/Y2024/01 Daily Notes" 
	and -#on/readme
SORT file.name DESC
LIMIT 15
```


For Each Year Update Following Settings
- DataView Query in Daily Notes (This page)
- Calendar/Metrics
	- Move it into Yearly Folder 
- In Built Plugin Settings
	- Daily Notes
		- New File Location: Calendar/Y2024/Daily Notes
- Community Plugin Settings
	- Periodic Notes
		- Daily
		- Weekly
		- Monthly
		- Quarterly
		- Yearly


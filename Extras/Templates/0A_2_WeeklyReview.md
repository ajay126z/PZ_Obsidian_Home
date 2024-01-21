---
up:
  - "[[2024-M01 (Jan)]]"
prev: 
next: 
tags:
  - "#Log/weekly"
created:
  - "{{date}} {{time}}"
updated: 2024-01-21T01:19
---

---
**Navigate Week Notes**:
	<< [[Invalid date | Previous Week]] ⇔ [[Invalid date | Next Week]] >>	

---

# WEEKLY METRICS OVERVIEW
## Journal Pages: Invalid date - Invalid date

```dataview
LIST
FROM "Calendar/Y2024/01 Daily Notes"
WHERE week-note = [[0A_2_WeeklyReview]]
SORT file.name ASC
```

## Exercise and Health

```dataview
TABLE WITHOUT ID
	file.link as "Day",
	Morning_Wakeup as "🌞",
	Suryanamaskar as "🙏",
	Meditation as "🧘",
	Workout as "🏋️"
FROM "Calendar/Y2024/01 Daily Notes"
WHERE week-note = [[0A_2_WeeklyReview]]
SORT file.link ASC
```

#### Tracker: Suryanamaskar, Meditation and Workout

```tracker
searchType: dvField
searchTarget: Suryanamaskar, Meditation, Workout
folder: Calendar/Y2024/01 Daily Notes
startDate: 2024-01-15 (W03-Mon)
endDate: 7d
datasetName: Suryanamaskar, Meditation, Workout
line:
    title: "0A_2_WeeklyReview: 🌞, 🧘‍♂️, 🏋️"
    lineColor: orange, white, red
    yAxisLabel: unit
    showLegend: true
```
##### Suryanamaskar Summary
```tracker
searchType: dvField
searchTarget: Suryanamaskar, Meditation
folder: Calendar/Y2024/01 Daily Notes
startDate: 2024-01-15 (W03-Mon)
endDate: 7d
summary:
    template: "|*******************|\n|** Suryanamaskar **|\n|*******************|\nTotal Rounds:{{sum()}}\nMaximum: {{max()}} rounds\nMinimum: {{min()}} rounds\nAverage: {{average()}} rounds"
```

##### Meditation Summary
```tracker
searchType: dvField
searchTarget: Meditation
folder: Calendar/Y2024/01 Daily Notes
startDate: 2024-01-15 (W03-Mon)
endDate: 7d
summary:
    template: "|*******************|\n|** Medidation **|\n|*******************|\nTotal Minutes:{{sum()}}\nMaximum: {{max()}} Minutes\nMinimum: {{min()}} Minutes\nAverage: {{average()}} Minutes"
```

#### Tracker: Rise, Shine and Set

```tracker
searchType: dvField
searchTarget: PZ_RiseSet[0], PZ_RiseSet[1]
startDate: 2024-01-15 (W03-Mon)
endDate: 7d
folder: Calendar/Y2024/01 Daily Notes
datasetName: Rise, Set
fixedScale: 1.2
line:
    title: "AZ Rise, Shine and Set"
    yAxisLabel: "Time (24h)"
    reverseYAxis: true
    lineColor: yellow, red
    showPoint: true
    showLegend: true
```

#### Tracker: Screen Time



## Foods

```dataview
TABLE WITHOUT ID
	file.link as "Day",
	Breakfast as "☕",
	Lunch as "🍱",
	Dinner as "🍲"
FROM "Calendar/Y2024/01 Daily Notes"
WHERE week-note = [[0A_2_WeeklyReview]]
SORT file.link ASC
```

### Weekly Meal Plan 0A_2_WeeklyReview

| Day | ☕ Breakfast | 🍱 Lunch | 🍵 Dinner |
| ---- | ---- | ---- | ---- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |



---
# 0A_2_WeeklyReview - WEEKLY PLANNING

## MIP 3 Goals
> [!question] Three goals
> - If you could only get three specific goals done this week, what would they be? 
> - How do they relate to your monthly initiatives and yearly OKRs?

- [ ] 
- [ ] 
- [ ] 

## Exploration Ideas

> [!tip] THINK BIGGER
> - What things are you excited about right now?
> - What new things do you want to learn?


---
# WEEKLY MEMOS and NOTES

## Weekly Memos List

## Notes Statistics

### Notes Created This Week

```dataview
TABLE WITHOUT ID 
	length(rows) as "Total Notes Created in 0A_2_WeeklyReview"
FROM ""
WHERE 
	file.cday >= date(2024-01-15) and file.cday <= date(2024-01-21)
GROUP BY true
```

### Notes Modified This Week
```dataview
TABLE WITHOUT ID 
	length(rows) as "Total Notes Modified in 0A_2_WeeklyReview"
FROM ""
WHERE 
	file.mday >= date(2024-01-15) and file.mday <= date(2024-01-21)
GROUP BY true
```


## Weekly Tasks List

> [!todo] TODO's in This Week. task Query

```dataview
TASK
FROM "Calendar/Y2024/01 Daily Notes" 
WHERE week-note = [[0A_2_WeeklyReview]]
```

----
# 📃 WEEKLY REFLECTION & CELEBRATION 

> [!summary] Reflect on this Week.
> - Review your completed tasks/goal/notes in this week.
> - What progress have you made on each of your top priorities?
> - What were your most important tasks and events this week?

## Projects
### LIST OF PROJECT[s] I worked on this week?
- 
### **TGR: What did I accomplish?**
- 
### **TGW: What setbacks did I face?**
- 
### **LEARNINGS: What are some possible improvements and plans for the future??**
- 

---
# PLANNING AHEAD

> [!note] Plan the Week Ahead
> - What progress have you made on each of your top priorities?
> - What needs to be updated?
> - What needs to happen next on each project or area? Clarify Next Action.
> - What are your most important tasks and events each day next week?


### Weekly Meal Plan -[[Invalid date]]

| Day | ☕ Breakfast | 🍱 Lunch | 🍵 Dinner |
| ---- | ---- | ---- | ---- |
| [[Invalid date]] |  |  |  |
| [[Invalid date]] |  |  |  |
| [[Invalid date]] |  |  |  |
| [[Invalid date]] |  |  |  |
| [[Invalid date]] |  |  |  |
| [[Invalid date]] |  |  |  |
| [[Invalid date]] |  |  |  |
|  |  |  |  |



---

# EXTRA THOUGHTS...



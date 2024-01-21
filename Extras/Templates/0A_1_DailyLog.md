---
up:
  - "[[Daily Notes]]"
week-note: '[[<% tp.date.now("YYYY-[W]ww") %>]]'
tags:
  - "#Log/daily"
created:
  - "{{date}} {{time}}"
updated: 2024-01-21T10:48
---

---
**Navigate Notes**:
	<< [[<% tp.date.now("YYYY-MM-DD ([W]ww-ddd)", -1) %> | Yesterday]] ⇔[[<% tp.date.now("YYYY-MM-DD ([W]ww-ddd)", 1) %> | Tomorrow]] >>	
	<<<< [[<% tp.date.now("YYYY-MM-DD", "P-1Y") %> | On this day 1 Year Ago]]

---
# 📅 Journal Entry {{date: YYYY-MM-DD ([W]WW-ddd)}}
---
---
## ⏳ Time Blocks Statistics
```dataviewjs
	// Get Current File Name
	const Current_file_name = dv.current().file.name;
		
	// Get Current Date
	const today_date = moment();	
	const currentDate = today_date.format('YYYY-MM-DD');

	// Update Block statistics based on File journal day.
	if(Current_file_name.includes(currentDate))
	{
		// Get Today Object
		const today = DateTime.now();
		
		// constant Variables
		const T10_total = 144;
		let T10_current = 0;
		
		// Variables for Day's progress
		let T10_total_use = T10_total;
		let T10_current_use = 0;
		let T10_remaining_use = 0;
		let Today_RemPct_use = 0;

		// Get Today's Current Time Block
		T10_current = (((today.hour * 6) + (today.minute/10)) | 0 ) + 1;
		
		if((today.hour >= 6) && (today.hour <= 22))
		{
			T10_total_use = T10_total - 36; // 6H Sleep (36 Blocks)
			
			T10_current_use = T10_current - 36;
			// Calculate Today's remaining Time Blocks
			T10_remaining_use = T10_total_use - T10_current_use;

			// Calculate remaining Day time in percentage (with accuracy in minutes).
		   Today_RemPct_use = (((today.hour * 60) +(today.minute) - 360) / (1440-360)) * 100;
		}
		else
		{
			T10_total_use = T10_total;
			T10_current_use = T10_current;
			
			// Calculate Today's remaining Time Blocks
			T10_remaining_use = T10_total_use - T10_current_use;

			// Calculate remaining Day time in percentage (with accuracy in minutes).
			Today_RemPct_use = (((today.hour * 60) +(today.minute)) / 1440) * 100;
		}
		
		// Render Current Date, time and progress 
		dv.paragraph("**Today**")
		dv.paragraph("*Today's Daily Note Name* &nbsp;: " + Current_file_name);
		dv.paragraph("*Date* &nbsp;: &nbsp;&nbsp;&nbsp; " + currentDate);
		dv.paragraph("*Time* &nbsp;: &nbsp;&nbsp;&nbsp; " + today.hour + ":" + today.minute)

		// Render Day Progress
		dv.paragraph(`**Day Progress **&nbsp;&nbsp;&nbsp;&nbsp; ⇨ &nbsp;&nbsp; <progress  value="${parseInt(Today_RemPct_use)}" max="100"></progress> ⌛ ${parseInt(Today_RemPct_use)} %`)

		// Create a table to show consolidate information of T30/T15/T10 time blocks.
		let arr = [ 
			["Total Blocks", parseInt(T10_total_use)],
			["Current Block", T10_current_use],
			["Remaining Blocks", parseInt(T10_remaining_use)]
		];

		dv.table(["Time Blocks", "T10 Blocks"], arr.map(v => v));
	}
	else
	{
		
		dv.paragraph("*Current Date* &nbsp;: **" + currentDate + "**");
		dv.paragraph(" Block statistics is not displayed for file *'" + Current_file_name + "'*. Because..., ");
		dv.paragraph("- Journal Day is passed! OR");
		dv.paragraph("- Journal Day is for future! OR");
		dv.paragraph("- This file is a template for Daily Journal! OR");
		 dv.paragraph("- This file is not related to Daily Journal! ");
	  }	
```
---
## 💪 Health Metrics
### [[🚀 Morning Routine]]
- PZ_Rise:: %%Habit-Morning_Wakeup%%
	- When did you wake up today?
-  Suryanamaskar:: %%Habit-Suryanamaskar_Status%%
	- Have you perform Suryanamaskar today? 
- Meditation:: %%Habit-Meditation_Mindfullness%%
	- Did you Meditate Today? 
-  Workout:: %%Habit-Exercise%%
	- Zumba Dance or Workout? 
- PZ_Set:: %%Habit-Evening_Sleep%%
	- When are you going to sleep today? Execute Shut Down Routine. 
###  [[🍲 Food Journal]]
- Breakfast:: 
- Lunch:: 
- Dinner::

---
---
## 🗒️ Notes 
- 

### 👷‍♂️ Tasks 
- 

---
---
## 🌝 Day Review

---
---

## 🗒️ Notes Statistics

### Notes Created on Today

```dataview
TABLE WITHOUT ID 
	file.link AS "File Name", 
	file.folder AS "File Path", 
	tags AS "Tags", 
	file.ctime AS "Created Time",
	file.mtime AS "Last Modified Time"
FROM ""
WHERE 
	file.cday = date(regexreplace(this.file.name, "^.*(\d\d\d\d-\d\d-\d\d).*$", "$1"))
SORT file.ctime DESC
```

### Notes Modified on Today

```dataview
TABLE WITHOUT ID 
	file.link as "File Name", 
	file.folder as "File Path", 
	tags as "TAGS", 
	file.mtime AS "Modified Time", 
	file.ctime AS "Created Time"
FROM ""

WHERE 
	file.mday = date(regexreplace(this.file.name, "^.*(\d\d\d\d-\d\d-\d\d).*$", "$1")) AND 
	file.cday != date(regexreplace(this.file.name, "^.*(\d\d\d\d-\d\d-\d\d).*$", "$1"))

SORT file.mtime DESC
```

---


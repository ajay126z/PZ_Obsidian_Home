---
aliases:
  - "000"
tags:
  - "#map/view"
  - "#mylife"
created: 2023-12-13T11:55
updated: 2024-01-21T00:59
---

# 🏡 Home 
Your launchpad and home base. That's here. That's home.

> [!idea] Reminder 
>  *There are people worse than you at everything, getting paid way more than you because they didn’t wait till they were “ready”.*

## 🚧 Life Progress
```dataviewjs
	const today = DateTime.now()
	const endOfYear = {
	    year: today.year,
	    month: 12,
	    day: 1
	}

	const lifespan = { year: 80 } 
	const birthday = DateTime.fromObject({
	    year: 1993,
	    month: 3,
	    day: 26
	});
	const deathday = birthday.plus(lifespan)
	
	function progress(type) {
	    let value;
	    
	    switch(type) {
	        case "lifespan": 
	            value = (today.year - birthday.year) / lifespan.year * 100;
	            break;
	        case "lifeRemaining":
		        value = (((lifespan.year + birthday.year) - today.year) / lifespan.year) * 100;
	            break;
	        case "year":
	            value = today.month / 12 * 100
	            break;
	        case "month":
	            value = today.day / today.daysInMonth * 100
	            break;
	        case "day":
	            value = today.hour / 24 * 100
	            break;
	    }
	    return `<progress value="${parseInt(value)}" max="100"></progress> ⌛ ${parseInt(value)} %`
	}

	dv.paragraph("---");
	dv.paragraph("**Today**")
	dv.paragraph("*Date* &nbsp;: &nbsp;&nbsp;&nbsp; " + today.year + "/" + today.month + "/" + today.day);
	dv.paragraph("*Time* &nbsp;: &nbsp;&nbsp;&nbsp; " + today.hour + ":" + today.minute)
	dv.paragraph("---");
	dv.paragraph("**Curr Year**&nbsp;&nbsp;&nbsp;&nbsp; ⇨ " + progress("year"));
	dv.paragraph("**Curr Month** ⇨ " + progress("month"));
	dv.paragraph("** Today**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ⇨ " + progress("day") );
	dv.paragraph("---");
	dv.paragraph("**Life Past**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  ⇨ " + progress("lifespan"));
	dv.paragraph("**Life Remaining**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  ⇨ " + progress("lifeRemaining"));
	dv.paragraph("---");
```


## 🗺️ Atlas 
These are maps to launch your `efforts`. Where would you like to go?

- My Main Sensemaking
	- 01 - [[Thinking MOC]]
	- 02 - **Input -> Process --> Output**
		- [[📥 Inbox]]
		- [[🗃️ Notebox]]
		- [[🔮 Outbox]]
	- 03 - [[Daily Notes]], [[Weekly Notes]] and [[Monthly Notes]]
	- 04 - [[🗓️ Calendar]] 
-  Things
	- 07 - [[Sources MOC]]
	- 08 - [[Concepts MOC]]
- Action and Reflection
	- 10 - [[Efforts]]
	- 11 - [[Plan and Review]]
	- 15 - [[My Projects]]
	- 13 - [[My Goals]]
	- 14 - [[My Habits]] and [[My Ideal Day]]
	- 09 - [[Digital_Garden_MOC]]
- Personal Management and Life Stuff
	- 15 - [[Life Map]]
	- 16 - [[Meta PKM]]
	- 17 - [[Health MOC]] 
	- 18 - [[Finance MOC]]
	- 20 - [[LYT Kit]], [[+ About Spaces]] and [[Meta PKM]]

![[pale-blue-dot-banner.jpg]]





---

## 📊 Folder Wise - Note Statistics

| Folder Name    | File Count                                 |
| -------------- | ------------------------------------------ |
| Encounter      | `$=dv.pages('"+ Encounters"').length`      |
| Atlas          | `$=dv.pages('"Atlas"').length`             |
| Calendar       | `$=dv.pages('"Calendar"').length`          |
| Cards          | `$=dv.pages('"Cards"').length`             |
| Extras         | `$=dv.pages('"Extras"').length`            |
| Sources        | `$=dv.pages('"Sources"').length`           |
| Spaces         | `$=dv.pages('"Spaces"').length`            |
| Excalidraw     | `$=dv.pages('"yDraw"').length`        |
| Digital Garden | `$=dv.pages('"ZenGarden"').length` |
| **Total**      | `$=dv.pages().length`                      |


---

## Life Perspective
- 


## 🗺️ Atlas
- [[People MOC]]
- ## References
	- [[My Ideal Day]]
	- [[My Role Models]]
	- [[Productivity Systems]]
		- [[🧰 My Tools]]
		- [[$Logseq]]
		- [[$Things3]]
	- [[Quotes]]
	- [[📥 Books Inbox]]
	- [[Best of TKMOC]]
- ## Review Process
	- [[Daily Review]]
	- [[Calendar/OKRs Templates/Weekly Review]]
	- [[Monthly Review]]
	- [[Quarterly Review]]
	- [[Annual Review]]
